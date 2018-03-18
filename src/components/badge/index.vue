<template>
  <span class="vux-badge" :class="{
    'vux-badge-dot': !text,
    'vux-badge-single': text && text.length === 1
  }">{{text}}</span>
</template>

<script>
export default {
  name: 'badge',
  props: {
    text: [String, Number]
  }
}
</script>

<style lang="less">
@import '../../styles/variable.less';

.vux-badge {
  display: inline-block;
  text-align: center;
  background: @badge-bg-color;
  color: #fff;
  font-size: 12px;
  height: 16px;
  line-height: 16px;
  border-radius: 8px;
  padding: 0 6px;
  background-clip: padding-box;
  vertical-align: middle;
}
.vux-badge-single {
  padding: 0;
  width: 16px;
}
.vux-badge-dot {
  height: auto;
  padding: 5px
}
</style>
