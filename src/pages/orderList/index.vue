<template>
  <div>
    <div class="container">
      <a
        class="link"
        v-for="(chart, index) of charts"
        :key="index"
        @click="navigate({path: chart.path})"
      >{{chart.config.navigationBarTitleText}}</a>
    </div>
    <ad unit-id="adunit-162e15806841e6e8"></ad>
  </div>
</template>
<script>

export default {
  data () {
    return {
      charts: [
        {
          'path': 'bar',
          'config': {
            'navigationBarTitleText': '柱状图'
          }
        },
        {
          'path': 'scatter',
          'config': {
            'navigationBarTitleText': '散点图'
          }
        },
        {
          'path': 'pie',
          'config': {
            'navigationBarTitleText': '饼图'
          }
        },
        {
          'path': 'line',
          'config': {
            'navigationBarTitleText': '折线图'
          }
        },
        {
          'path': 'funnel',
          'config': {
            'navigationBarTitleText': '漏斗图'
          }
        },
        {
          'path': 'gauge',
          'config': {
            'navigationBarTitleText': '仪表盘'
          }
        },
        {
          'path': 'k',
          'config': {
            'navigationBarTitleText': '线图'
          }
        },
        {
          'path': 'radar',
          'config': {
            'navigationBarTitleText': '雷达图'
          }
        },
        {
          'path': 'heatmap',
          'config': {
            'navigationBarTitleText': '热力图'
          }
        },
        {
          'path': 'tree',
          'config': {
            'navigationBarTitleText': '树图'
          }
        },
        {
          'path': 'treemap',
          'config': {
            'navigationBarTitleText': '矩形树图'
          }
        },
        {
          'path': 'sunburst',
          'config': {
            'navigationBarTitleText': '旭日图'
          }
        },
        {
          'path': 'map',
          'config': {
            'navigationBarTitleText': '地图'
          }
        },
        {
          'path': 'graph',
          'config': {
            'navigationBarTitleText': '关系图'
          }
        },
        {
          'path': 'boxplot',
          'config': {
            'navigationBarTitleText': '箱型图'
          }
        },
        {
          'path': 'parallel',
          'config': {
            'navigationBarTitleText': '平行坐标图'
          }
        },
        {
          'path': 'sankey',
          'config': {
            'navigationBarTitleText': '桑基图'
          }
        },
        {
          'path': 'themeRiver',
          'config': {
            'navigationBarTitleText': '主题河流图'
          }
        },
        {
          'path': 'lazyLoad',
          'config': {
            'navigationBarTitleText': '延迟加载图表'
          }
        },
        {
          'path': 'multiCharts',
          'config': {
            'navigationBarTitleText': '一个页面中多个图表'
          }
        }
      ]
    }
  },
  methods: {
    navigate (params) {
      this.$navigateTo('demos', params)
    }
  }
}
</script>
<style scoped>
.container {
   height: 100vh;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10rpx 0;
  box-sizing: border-box;
  flex-wrap: wrap;
  background-color: #fff;
}
.link {
  width: 50%;
  text-align: center;
  padding: 10px 0;
}
</style>
