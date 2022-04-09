<script>
import { Line } from "vue-chartjs";
export default {
    name:"LinerChartPercent",
  extends: Line,
  
data(){
  return{
    chartData:{
      labels:["فروردین","اردیبهشت","خرداد","تیر"],
      datasets:[{
        label:" %درصد پیشرفت",
        borderColor:"#4bcc96",
        borderWidrh:4,
        pointBackgroundColor:"#000",
        pointRadius:5,
        pointHoverBorderColor:"#000",
        fill:false,
        data:[0,10,12,18]
      }]
    },
    options:{
      maintainAspectRatio:false,
      responsive:true,
      tooltips:{
        backgroundColor:"#000",
        titleFontColor:"#ffffff",
        bodyFontColor:"#ffffff",
        position:"nearest",
        mode:"nearest",
        intersect:0,
        bodySpacing:4,
        xPadding:20,

      }

    }
  }
},


  mounted() {
    this.renderChart(this.chartData, this.options);
  },
};
</script>

<style>

</style>
