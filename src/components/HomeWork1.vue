<template>
  <div :class="[$style.box, $style.center]">
    <!--  -->
    <h2 :class="$style.text">Домашняя работа</h2>

    <div :class="$style.conteiner">
      <img :src="product.img" alt="foto" :class="$style.img" />
      <div>
        <p>{{ product.name }}</p>
        <p>Стоимость товара: {{ formattedPrice }}</p>
        <p>{{ availableProduct() }}</p>
      </div>
    </div>

    <!--  -->
  </div>
</template>

<script>
export default {
  name: "HomeWork1",

  data() {
    return {
      product: {
        name: "Яблоки",
        price: 95,
        available: true,
        quantity: 10,
        img: "./img/apple.png",
      },
    };
  },

  computed: {
    formattedPrice() {
      return this.product.price + " руб";
    },
  },

  mounted() {},

  methods: {
    availableProduct() {
      if (Number(this.product.quantity) <= 10 && Number(this.product.quantity) > 4) {
        return 'Товара достаточно в наличии'
      } else if (Number(this.product.quantity) <= 4 && Number(this.product.quantity) > 0) {
        return 'Товар заканчивается'
      } else {
        this.product.available = false
        return 'Товара  нет в ниличии'
      }
    },
  },
};
</script>

<style lang="scss" module>
.center {
  padding-right: calc(50% - 500px);
  padding-left: calc(50% - 500px);
}
.box {
  margin-bottom: 150px;
}

.text {
  color: blue;
}

.conteiner {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  gap: 20px;
}
.img {
  width: 200px;
}
</style>

<!-- Вы разрабатываете приложение для интернет-магазина 
    и у вас есть компонент Vue под названием "ProductDetails". 
    Компонент отображает детали о конкретном продукте, включая его название, цену и статус доступности.

Внутри компонента "ProductDetails" создайте свойство "product" с объектом, 
представляющим информацию о продукте.
 Объект должен иметь свойства "name" (название продукта), 
 "price" (цена продукта) 
 и "available" (флаг, указывающий на доступность продукта).

 Используя вычисляемое свойство, назовите его "formattedPrice", 
 которое будет возвращать форматированную цену продукта со знаком валюты. 
 Например, если цена равна 99.99, вычисляемое свойство должно вернуть строку "$99.99".
В компоненте "ProductDetails" отобразите название продукта, его форматированную цену и статус доступности.
Если продукт доступен, отобразите текст "Available", в противном случае - "Out of stock". -->
