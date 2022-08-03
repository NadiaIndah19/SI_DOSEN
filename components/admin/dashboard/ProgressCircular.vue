<template>
  <div>
    <base-card size="s" class="px-3 py-4">
      <div class="d-flex">
        <v-icon> mdi-domain </v-icon>
        <v-card-title
          class="py-3 px-3 light-blue--text text--darken-4"
          >Data Dosen
        </v-card-title>
      </div>
      <v-divider />

      <v-row justify="space-between" class="py-4 px-2">
        <template v-for="(item, i) in dataCircular">
          <v-col
            class="d-flex flex-column justify-center align-center"
            cols="2"
            :key="`item-${i}`"
          >
            <v-progress-circular
              :rotate="360"
              :size="100"
              :width="15"
              :value="item.value"
              :color="item.color"
            >
              {{ item.value }}
            </v-progress-circular>
            <v-card-subtitle
              :class="`py-3 px-3 ${item.color}--text font-weight-bold text-center`"
              >{{ item.name }}
            </v-card-subtitle>
          </v-col>
        </template>
      </v-row>
    </base-card>
  </div>
</template>

<script>
export default {
  name: 'DashboardProgressCircular',
  data() {
    return {
      dataCircular: [
        { id: 1, name: 'Teknik Elektro', color: 'teal', value: 60 },
        {
          id: 2,
          name: 'Teknik Informatika dan Komputer',
          color: 'red',
          value: 10
        },
        { id: 3, name: 'Teknik Mekanik dan Energi', color: 'blue', value: 23 },
        { id: 4, name: 'Teknik Multimedia Kreatif', color: 'green', value: 52 },
        { id: 5, name: 'Pascasarjana', color: 'pink', value: 0 },
        { id: 6, name: 'Pendidikan Jarak Jauh', color: 'grey', value: 0 }
      ]
    }
  }
}
</script>
