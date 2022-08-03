<template>
  <div>
    <base-card size="s" class="px-3 py-4">
      <div class="d-flex justify-space-between">
        <v-card-title class="py-3 px-3 light-blue--text text--darken-4"
          >Dosen Politeknik Elektronika Negeri Surabaya
        </v-card-title>
        <v-card-title class="py-3 px-3 black--text font-weight-bold"
          >25
        </v-card-title>
      </div>
      <v-divider />

      <div class="py-4">
        <template v-for="(item, i) in dataLinear">
          <div :key="i">
            <div class="d-flex justify-space-between">
              <v-card-subtitle
                :class="`py-3 px-3 ${item.color}--text font-weight-bold text-center`"
                >{{ item.name }}
              </v-card-subtitle>
              <v-card-subtitle
                :class="`py-3 px-3 ${item.color}--text font-weight-bold text-center`"
                >{{ item.value }}
              </v-card-subtitle>
            </div>
            <v-progress-linear
              :color="item.color"
              :value="item.value"
            ></v-progress-linear>
          </div>
        </template>
      </div>
    </base-card>
  </div>
</template>

<script>
export default {
  name: 'DashboardProgressLinear',
  data() {
    return {
      dataLinear: [
        { id: 1, name: 'Total Dosen Laki - Laki', color: 'blue', value: 110 },
        {
          id: 2,
          name: 'Total Dosen Perempuan',
          color: 'red',
          value: 80
        }
      ]
    }
  }
}
</script>
