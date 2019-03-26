<template>
  <div>
    <div class="container">
      <div id="root" v-if="type!==''">
        <bar v-if="type === 'bar'"></bar>
        <scatter v-if="type === 'scatter'"></scatter>
        <pie v-if="type === 'pie'"></pie>
        <line v-if="type === 'line'"></line>
        <funnel v-if="type === 'funnel'"></funnel>
        <k v-if="type === 'k'"></k>
        <radar v-if="type === 'radar'"></radar>
        <heatmap v-if="type === 'heatmap'"></heatmap>
        <tree v-if="type === 'tree'"></tree>
        <treemap v-if="type === 'treemap'"></treemap>
        <sunburst v-if="type === 'sunburst'"></sunburst>
        <map v-if="type === 'map'"></map>
        <graph v-if="type === 'graph'"></graph>
        <boxplot v-if="type === 'boxplot'"></boxplot>
        <parallel v-if="type === 'parallel'"></parallel>
        <sankey v-if="type === 'sankey'"></sankey>
        <themeRiver v-if="type === 'themeRiver'"></themeRiver>
        <lazyLoad v-if="type === 'lazyLoad'"></lazyLoad>
        <multiCharts v-if="type === 'multiCharts'"></multiCharts>
      </div>
    </div>
  </div>
</template>

<script>
import bar from '../../components/bar'
import scatter from '../../components/scatter'
import pie from '../../components/pie'
import line from '../../components/line'
import funnel from '../../components/funnel'
import k from '../../components/k'
import radar from '../../components/radar'
import heatmap from '../../components/heatmap'
import tree from '../../components/tree'
import treemap from '../../components/treemap'
import sunburst from '../../components/sunburst'
import map from '../../components/map'
import graph from '../../components/graph'
import boxplot from '../../components/boxplot'
import parallel from '../../components/parallel'
import sankey from '../../components/sankey'
import themeRiver from '../../components/themeRiver'
import lazyLoad from '../../components/lazyLoad'
import multiCharts from '../../components/multiCharts'
export default {
  data () {
    return {
      type: ''
    }
  },
  components: {bar, scatter, pie, line, funnel, k, radar, heatmap, tree, treemap, sunburst, map, graph, boxplot, parallel, sankey, themeRiver, lazyLoad, multiCharts},

  mounted () {
    this.type = this.$root.$mp.query.path
  },
  methods: {}
}
</script>
<style scoped>
</style>
