<template>
  <div class="wrap">
    <check-icon :value.sync="demo1"> 同意不？({{ demo1 }})</check-icon>
      <br>
      <br>
    <check-icon :value.sync="demo2" type="plain"> 同意不？({{ demo2 }})</check-icon>
  </div>
</template>

<script>
import CheckIcon from 'mpvux/check-icon'

export default {
  components: {
    CheckIcon
  },
  methods: {
  },
  data () {
    return {
      demo1: false,
      demo2: true
    }
  }
}
</script>

<style lang="less">
</style>
