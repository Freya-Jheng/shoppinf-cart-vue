<template>
  <div class="wrapper">
    <div class="shopping-cart">
        <div class="cart-title">購物籃</div>
        <div class="carts-container">
          <div v-for="item in items" :key="item.id" class="cart">
            <img src="" alt="">
            <div class="product-description">
              <div class="product-unit">
                <span class="product-name">{{item.title}}</span>
                <div class="units-count">
                  <button type="button" class="minus unit-controller">-</button>
                  <div class="unit ">0</div>
                  <button type="button" class="add unit-controller">+</button>
                </div>
              </div>
              <div class="product-price">$<span class="first-price price-number sub-price">{{item.price}}</span></div>
            </div>
          </div>
        </div>
        <div class="total">
          <div class="total-shipping-fee">
            <span class="item">
              運費
            </span>
            <span class="price">
              $<span class="total-shipping-price sub-price">0</span>
            </span>
          </div>
          <div class="total-shipping-fee">
            <span class="item">
              小計
            </span>
            <span class="price">
              $<span class="total-price">0</span>
            </span>
          </div>
        </div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'Shopping Carts',
  props: {
    items: {
      type: Array,
      required: true,
    }
  },
  data () {
    return {
      // paint1: require('../statics/paint1.jpg')
    }
  }
}
</script>
<style scoped>
.wrapper {
  width: 45%;
}
</style>
