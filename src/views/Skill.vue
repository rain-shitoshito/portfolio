<template>
  <div>
    <bar-chart :chartdata="lang.chartdata" :options="lang.options"/>
    <p>Golangが今後伸びそうなので使おうと思う。</p>
    <bar-chart :chartdata="framework.chartdata" :options="framework.options"/>
    <p>vueとdjango rest frameworkでSPAを作ってみたい。あとGolangのginも。</p>
  </div>
</template>

<script>
import BarChart from "@/components/BarChart.vue";

export default {
  components: {
    "bar-chart": BarChart,
  },
  data(){
    return {
        lang: {
          chartdata: {
            labels: ["C", "C#", "python3", "javascript", "PHP", "html5", "css3"],
            datasets: [{
                label: "言語の習得度",
                data: [50, 55, 75, 75, 20, 70, 70],
                backgroundColor: [
                    "rgba(85, 85, 85, 0.2)",
                    "rgba(23, 134, 0, 0.2)",
                    "rgba(53, 114, 165, 0.2)",
                    "rgba(241, 224, 90, 0.2)",
                    "rgba(79, 93, 149, 0.2)",
                    "rgba(228, 75, 35, 0.2)",
                    "rgba(86, 61, 124, 0.2)",
                    
                ],
                borderColor: [
                    "#555555",
                    "#178600",
                    "#3572A5",
                    "#f1e05a",
                    "#4F5D95",
                    "#e44b23",
                    "#563d7c",
                ],
                borderWidth: 1
            }]
          },
          options: {
            responsive: true,
            maintainAspectRatio: false,
            scales: {
              xAxes: [{
                ticks: {
                  beginAtZero:true,
                  min: 0,
                  max: 100
                }
              }]
            }
          }
        },
        framework: {
          chartdata: {
            labels: ["Django", "Vue.js"],
            datasets: [{
                label: "フレームワークの習得度",
                data: [65, 30],
                backgroundColor: [
                    "rgba(85, 85, 85, 0.2)",
                    "rgba(23, 134, 0, 0.2)",
                    
                ],
                borderColor: [
                    "#555555",
                    "#178600",
                ],
                borderWidth: 1
            }]
          },
          options: {
            responsive: true,
            maintainAspectRatio: false,
            scales: {
              xAxes: [{
                ticks: {
                  beginAtZero:true,
                  min: 0,
                  max: 100
                }
              }]
            }
          }
        }
      }
    }
}
</script>