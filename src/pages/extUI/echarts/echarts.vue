<template>
  <view id="chart-container" style="width: 600px; height: 600px" />
</template>

<script>
import * as echarts from 'echarts';

export default {
  components: {},
  data() {
    return {};
  },
  mounted() {
    this.init();
  },
  methods: {
    init() {
      // 基于准备好的dom，初始化echarts实例
      console.log(echarts);
      var myChart = echarts.init(document.getElementById("chart-container"));
      // 指定图表的配置项和数据
      var option = {
        title: {
          text: "ECharts 入门示例",
        },
        tooltip: {},
        legend: {
          data: ["销量"],
        },
        xAxis: {
          data: ["衬衫", "羊毛衫", "雪纺衫", "裤子", "高跟鞋", "袜子"],
        },
        yAxis: {},
        series: [
          {
            name: "销量",
            type: "bar",
            data: [5, 20, 36, 10, 10, 20],
          },
        ],
      };
      // 使用刚指定的配置项和数据显示图表。
      myChart.setOption(option);
    },
  },
};
</script>

<style lang="scss">
.warp {
  padding: 10px;
}

.button {
  margin-bottom: 10px;
}
</style>
