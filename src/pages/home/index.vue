<template>
<div class="container">
  <a
    class="link"
    :class="{
      'done': page.status === 'done',
      'doing': page.status === 'doing'
    }"
    v-for="page of pages"
    :key="page.path"
    :href="'/' + page.path">{{page.name}}</a>
</div>
</template>

<script>
import pages from '../index'

export default {
  data () {
    return {
      pages
    }
  }
}
</script>

<style lang="less">
.link {
  width: 50%;
  text-align: center;
  padding: 10px;
  box-sizing: border-box;
  &.doing {
    color: #fff;
    background-color: rgb(127, 246, 255);
  }
  &.done {
    color: #fff;
    background-color: #60e460;
  }
}
</style>
