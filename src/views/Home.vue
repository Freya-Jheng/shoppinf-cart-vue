<template>
  <div class="wrapper">
    <!-- Checkout -->
    <Checkout />
    <!-- Shopping-Carts -->
    <ShoppingCart :items="items" />
  </div>
</template>

<script>
import Checkout from '../components/Checkout.vue'
import ShoppingCart from '../components/ShoppingCart.vue'
import uuid from 'uuid/v4'

const cartItems = {
  items: [
    {
      id: uuid(),
      title: '破壞補丁修身牛仔褲',
      image: ' ',
      price: '3999'
    },
    {
      id: uuid(),
      title: '刷色直筒牛仔褲',
      image: ' ',
      price: '1299'
    }
  ]
}

export default {
  name: 'Home',
  components: {
    Checkout,
    ShoppingCart,
  },
  data () {
    return {
      items: [],
    }
  },
  created () {
    this.fetchCartItems()
  },
  methods: {
    fetchCartItems(){
      const {items} = cartItems
      this.items = items
    }
  }
}
</script>


<style scoped>

.wrapper {
  /* border: 3px solid red; */
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
