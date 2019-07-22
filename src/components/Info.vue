<template>
  <div class="container">
    <div class="item-wrapper">
      <div class="item">
        总数：
        <strong>{{totalNum}}</strong>
        <!-- 以下也是可以用的 -->
        <!-- <strong>{{this.$store.getters.totalNum}}</strong> -->
      </div>
      <div class="item">
        总价：
        <strong>{{totalPrice}}</strong>
      </div>
      <div @click="clearAllCart">清空购物车</div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
import { mapGetters, mapActions } from 'vuex'
export default {
  name: 'Info',
  mixins: [],
  components: {},
  props: {},
  data () {
    return {}
  },
  computed: {
    ...mapGetters(['totalPrice','totalNum'])
  },
  watch: {},
  methods: {
    ...mapActions(['clearAllCart'])
  },
  filters: {},
  mounted () { },
  created () { }
}
</script>

<style scoped>
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
