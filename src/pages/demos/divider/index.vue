<template>
  <div class="wrap">
    <divider>{{text}}</divider>
  </div>
</template>

<script>
import divider from 'mpvux/divider'

export default {
  components: {
    divider
  },
  methods: {
  },
  data () {
    return {
      text: '我是有底线的'
    }
  }
}
</script>

<style lang="less">
</style>
