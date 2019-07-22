<template>
  <div class="product">
    <h4>商品信息</h4>
    <table>
      <thead>
        <tr>
          <th>id</th>
          <th>名称</th>
          <th>价格</th>
          <th>操作</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(shop, index) in shopList" :key="index">
          <td>{{shop.id}}</td>
          <td>{{shop.name}}</td>
          <td>{{shop.price}}</td>
          <td>
            <div @click="addToCart(shop)" class="btn btn-info">购物车</div>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script type="text/ecmascript-6">
// 引入vuex
import { mapGetters, mapActions} from 'vuex'
export default {
  name: 'Product',
  mixins: [],
  components: {},
  props: {},
  data () {
    return {}
  },
  computed: {
    // 将vuex.getters中的shopList转为此处computed的属性shopList
    ...mapGetters(['shopList'])
  },
  watch: {},
  methods: {
    // 将`this.addToCart映射为this.$store.dispatch('addToCart')`
    ...mapActions(['addToCart'])
  },
  filters: {},
  mounted () { },
  created () { }
}
</script>

<style scoped>
  .table-shop > th {
    text-align: center;
  }
  .item-wrapper {
    display: flex;
    background-color: #dfdfdf;
    align-items: center;
    justify-content: center;
  }
  .item {
    flex: 1;
  }
</style>
