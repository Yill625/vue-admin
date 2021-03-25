<template>
  <div ref="demo" style="height:80vh;width:100%;" />
</template>
<script>
import * as echarts from 'echarts'

export default {
  name: 'Demo',
  mounted() {
    // 基于准备好的dom，初始化echarts实例
    var myChart = echarts.init(this.$refs.demo)
    // 绘制图表
    myChart.setOption({
      title: {
        text: 'ECharts示例'
      },
      tooltip: {},
      xAxis: {
        data: ['衬衫', '羊毛衫', '雪纺衫', '裤子', '高跟鞋', '袜子']
      },
      yAxis: {},
      series: [{
        name: '销量',
        type: 'bar',
        data: [5, 20, 36, 10, 10, 20]
      }]
    })
  }
}
</script>
