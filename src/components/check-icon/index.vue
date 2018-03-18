<template>
  <div class="vux-check-icon" @click="updateValue">
    <icon type="success" v-if="type === 'default' && value"></icon>
    <icon type="success_circle" v-if="type === 'plain' && value"></icon>
    <icon type="circle" v-if="!value"></icon>
    <span><slot></slot></span>
  </div>
</template>

<script>
import Icon from '../icon'

export default {
  name: 'check-icon',
  components: {
    Icon
  },
  methods: {
    updateValue () {
      this.$emit('update:value', !this.value)
    }
  },
  props: {
    value: {
      type: Boolean,
      default: false
    },
    type: {
      type: String,
      default: 'default'
    }
  }
}
</script>

<style lang="less">
@import '../../styles/variable.less';

.vux-check-icon {
  display: inline-block;
}
.vux-check-icon > .weui-icon-circle {
  line-height: 23px;
  color: #222;
  vertical-align: middle;
}
.vux-check-icon > .weui-icon-success:before, .vux-check-icon > .weui-icon-success-circle:before {
  color: @check-icon-color-checked;
}
</style>
