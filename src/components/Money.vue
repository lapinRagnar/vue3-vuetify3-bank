<template>

  <v-card color="#202022" class="rounded-lg">

    <v-row>

      <v-col cols="12" sm="8">

        <v-toolbar color="transparent" class="">
          <v-toolbar-title>
            Money Earned From
          </v-toolbar-title>

          <v-spacer></v-spacer>

          <span class="text-grey">1 Year</span>

          <v-icon color="#878A94" class="ml-2" size="x-small">fas fa-chevron-down</v-icon>


        </v-toolbar>

        <!-- <Scatter
          :chart-options="chartOptions"
          :chart-data="chartData"
          :chartId="chartId"
          :dataset-id-key="datasetIdKey"
          :plugins="plugins"
          :css-classes="cssClasses"
          :styles="styles"
          :width="width"
          :height="height"
        >

        </Scatter> -->

      </v-col>

    </v-row>
  </v-card>

</template>

<script>

  import { Scatter } from "vue-chartjs/legacy"

  import {
    Chart as ChartJS,
    Title,
    Tooltip,
    Legend,
    LineElement,
    LinearScale,
    CategoryScale,
    PointElement,
  } from "chart.js"

  ChartJS.register(
    Title,
    Tooltip,
    Legend,
    LineElement,
    LinearScale,
    CategoryScale,
    PointElement
  )

  export default {
    props: {
      chartId: {
        type: String,
        default: "scatter-chart",
      },
      datasetIdKey: {
        type: String,
        default: "label",
      },
      width: {
        type: Number,
        default: 400,
      },
      height: {
        type: Number,
        default: 180,
      },
      cssClasses: {
        default: "",
        type: String,
      },
      styles: {
        type: Object,
        default: () => {},
      },
      plugins: {
        type: Array,
        default: () => [],
      },
    },
    data: () => ({
      chartData: {
        datasets: [
          {
            label: "S41k/ Income",
            fill: false,
            borderColor: "#f87979",
            backgroundColor: "#f87979",
            data: [
              {
                x: -2,
                y: 4,
              },
              {
                x: -1,
                y: 1,
              },
              {
                x: 0,
                y: 0,
              },
              {
                x: 1,
                y: 1,
              },
              {
                x: 2,
                y: 4,
              },
            ],
          },
          {
            label: "Banking",
            fill: false,
            borderColor: "#524EED",
            backgroundColor: "#524EED",
            data: [
              {
                x: -2,
                y: -4,
              },
              {
                x: -1,
                y: -1,
              },
              {
                x: 0,
                y: 1,
              },
              {
                x: 1,
                y: -1,
              },
              {
                x: 2,
                y: -4,
              },
            ],
          },
        ],
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false,
      },
      /* files */
      files: [
        {
          color: "blue",
          icon: "fas fa-dollar-sign",
          subtitle: "Dolars",
          title: "24",
        },
        {
          color: "green",
          icon: "fas fa-pound-sign",
          subtitle: "Pound ",
          title: "24",
        },
        {
          color: "orange",
          icon: "fas fa-euro-sign",
          subtitle: "Euro",
          title: "24",
        },
      ],
    }),
    components: {
      Scatter,
    },
  }

</script>

<style lang="scss">

</style>
