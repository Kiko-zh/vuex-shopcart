<template>
  <div class="container">
    <h4>已选商品</h4>
    <table>
      <thead>
        <tr>
          <th>id</th>
          <th>名称</th>
          <th>价格</th>
          <th>数量</th>
          <th>操作</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(shop, index) in cartProducts" :key="index">
          <td>{{shop.id}}</td>
          <td>{{shop.name}}</td>
          <td>{{shop.price}}</td>
          <td>{{shop.num}}</td>
          <td>
            <div @click="delProduct(shop)">删除</div>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script type="text/ecmascript-6">
import {mapGetters, mapActions} from 'vuex'
export default {
  name: 'Cart',
  mixins: [],
  components: {},
  props: {},
  data () {
    return {}
  },
  computed: {
    ...mapGetters(['cartProducts'])
  },
  watch: {},
  methods: {
    ...mapActions(['delProduct'])
  },
  filters: {},
  mounted () { },
  created () { }
}
</script>

<style scoped>
</style>
