<template>
<div>
    <base-card size="s" class="px-3 py-4">
      <div class="d-flex justify-space-between">
        <v-card-title class="py-3 px-3 light-blue--text text--darken-4"
          >Jenjang Pendidikan
        </v-card-title>
      </div>
      <v-divider />

      <Bar
      :chart-options="chartOptions"
      :chart-data="chartData"
      :chart-id="chartId"
      :dataset-id-key="datasetIdKey"
      :plugins="plugins"
      :css-classes="cssClasses"
      :styles="styles"
      :width="width"
      :height="height"
    />
    </base-card>
  </div>
</template>

<script>
import { Bar } from 'vue-chartjs/legacy'
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  BarElement,
  CategoryScale,
  LinearScale
} from 'chart.js'

ChartJS.register(
  Title,
  Tooltip,
  Legend,
  BarElement,
  CategoryScale,
  LinearScale
)

ChartJS.defaults.color = '#000000'

export default {
  name: 'BaseBarChart',
  components: { Bar },
  props: {
    title: {
      type: String,
      default:
        'Total Dosen'
    },
    chartId: {
      type: String,
      default: 'bar-chart'
    },
    datasetIdKey: {
      type: String,
      default: 'label'
    },
    width: {
      type: Number,
      default: 400
    },
    height: {
      type: Number,
      default: 200
    },
    cssClasses: {
      default: '',
      type: String
    },
    styles: {
      type: Object,
      default: () => {}
    },
    plugins: {
      type: Object,
      default: () => {}
    }
  },
  data() {
    return {
      chartData: {
        labels: [
          'S2',
          'S3'
        ],
        datasets: [
          {
            label: 'Jenjang Pendidikan',
            data: [
              200, 120
            ],
            backgroundColor: [
              'red',
              'blue'
            ]
          }
        ]
      },
      chartOptions: {
        responsive: true
      }
    }
  }
}
</script>

<style scoped>
.neumorphism-shadow {
  box-shadow: -6px -6px 12px #ffffff,
    6px 6px 12px
      rgba(111, 112, 113, 0.8);
  border-radius: 10px;
}
</style>
