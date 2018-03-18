<template>
  <div class="wrap">
    <div class="badge">
      <badge />
    </div>
    <div class="badge">
      <badge text="1" />
    </div>
    <div class="badge">
      <badge text="哈哈哈" />
    </div>
  </div>
</template>

<script>
import badge from 'mpvux/badge'

export default {
  components: {
    badge
  },
  methods: {
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="less">
.badge {
  margin: 0 10px;
}
</style>
