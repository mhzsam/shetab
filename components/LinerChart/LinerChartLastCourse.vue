<script>
import { Line } from "vue-chartjs";
export default {
    name:"LinerChartLastCourse",
  extends: Line,
  
data(){
  return{
    chartData:{
      labels:["فروردین","اردیبهشت","خرداد"],
      datasets:[{
        label:" %درصد پیشرفت",
        borderColor:"#d534eb",
        borderWidrh:4,
        pointBackgroundColor:"#000",
        pointRadius:5,
        pointHoverBorderColor:"#000",
        fill:false,
        data:[0,65,98]
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
