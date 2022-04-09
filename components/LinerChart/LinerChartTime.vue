<script>
import { Bar } from "vue-chartjs";
export default {
  name: "LinerChartTime",
  extends: Bar,

  data() {
    return {
      chartData: {
        labels: [
          "شنبه",
          "یک شنبه",
          "دوشنبه",
          "سه شنبه",
          "چهار شنبه",
          "پنج شنبه ",
          "جمعه",
        ],
        datasets: [
          {
            label: " بر حسب دقیقه",
            borderColor: "#19b351",
            backgroundColor: "#03fc56",
            borderWidth: 2,
            pointBackgroundColor: "#000",
            pointRadius: 5,
            pointHoverBorderColor: "#000",
            
            data: [10, 65, 15, 22, 35, 5, 0],
          },
        ],
      },
      options: {
        
        maintainAspectRatio: false,
        responsive: true,
        tooltips: {
          backgroundColor: "#000",
          titleFontColor: "#ffffff",
          bodyFontColor: "#ffffff",
          position: "nearest",
          mode: "nearest",
          intersect: 0,
          bodySpacing: 4,
          xPadding: 20,
          
        },
      },
    };
  },

  mounted() {
    this.renderChart(this.chartData, this.options);
  },
};
</script>

<style></style>
