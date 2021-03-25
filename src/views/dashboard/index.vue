<template>
  <div class="dashboard-container">
    <Demo />
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import Demo from '@/components/Echarts/demo'

export default {
  name: 'Dashboard',
  components: {
    Demo
  },
  computed: {
    ...mapGetters([
      'name'
    ])
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
