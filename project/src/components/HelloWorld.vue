<template>          
    <div>
        <div id="mapContainer" style="width:600px; height:600px"></div>
    </div>
</template>
        
<script>
    import option from './map-option'  //引入配置项
    require('./../../node_modules/echarts/map/js/china.js')  //引入china.js地图文件

    export default {
        name: 'hello',
        data () {
          return {  
          }
        },
        methods: {
          drawChinaMap() {
            var myChart = this.$echarts.init(document.getElementById('mapContainer'));
            myChart.setOption(option);
          }
        },
        mounted() {
          this.drawChinaMap();
        }
    }
</script>
        
<style scoped>
       
</style>