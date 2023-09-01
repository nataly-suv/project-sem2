<template>
  <div :class="$style.box">
    <!-- 
         -->
    <h2 :class="$style.text">Корзина товаров</h2>
    <div v-for="(product, index) in products" :key="index">
      <input type="number" v-model.number="product.num" />
      <p>Название: {{ product.name }}</p>
      <p>Цена: {{ product.price }}</p>
      <p>Итоговая цена: {{ product.price * product.num }}</p>
    </div>
    <p>Итоговая цена {{ totalPrice }}</p>

   
    <!--             
         -->
  </div>
</template>

<script>
export default {
  name: "Task2Sem2",

  data() {
    return {
      products: [
        { name: "молоко", price: 95, num: 0 },
        { name: "хлеб", price: 46, num: 0  },
      ], 
      
    };
  },

  computed: {
    totalPrice () {
        return this.products.reduce( (total, item) => (total+item.price*item.num), 0);
    }, 

  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" module>
.box {
  margin-bottom: 150px;
}
.text {
  color: blue;
}
</style>
