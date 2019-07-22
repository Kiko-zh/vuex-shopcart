<template>
  <div id="app">
    <h3>Vuex购物车</h3>
    <!-- 商品列表 -->
    <product></product>
    <!-- 购物车列表 -->
    <Cart></Cart>
    <br />
    <!-- 小记 -->
    <Info></Info>
  </div>
</template>

<script>
import Product from './components/Product'
import Cart from './components/Cart'
import Info from './components/Info'
export default {
  name: 'app',
  components: {
    Product,
    Cart,
    Info
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
