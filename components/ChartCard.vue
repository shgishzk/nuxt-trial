<template>
  <v-card>
    <v-card-title>
      Pressure Chart
    </v-card-title>

    <v-card-text class="chart-container">
      <ChartCardStore :chartData="chartData" :options="options"/>
    </v-card-text>
  </v-card>
</template>

<script>
import ChartCardStore from './LineChart.vue';
export default {
    components: {
        ChartCardStore
    },
    data() {
        return {
            chartData: {
                labels: this.$store.state.chart.pressures.label,
                datasets: [{
                    label: "Pressure",
                    data: this.$store.state.chart.pressures.data,
                    fill: true,
                    backgroundColor: 'rgba(46, 170, 232, 0.4)',
                    borderColor: '#ABE1FA'
                }]
            },

            options: {
                responsive: true,
                maintainAspectRatio: false,
                legend: {
                    display: true
                },
            }
        }
    },
}
</script>
