<template>
  <v-container class="py-6 my-4">
    <!-- <v-row justify="end">
      <base-card size="s" color="light-blue darken-4" class-name="my-6 mx-2">
        <v-btn class="transparent" elevation="0">
          <v-card-subtitle class="py-1 px-3 white--text font-weight-bold"
            >Excel
          </v-card-subtitle>
        </v-btn>
      </base-card>
    </v-row> -->

    <!-- TOtal Card -->
    <div class="my-8">
      <v-row>
        <template v-for="(item, i) in totalData">
          <v-col :key="`item-${i}`">
            <AdminDashboardTotalCard
              :name="item.name"
              :total-data="item.totalData"
              :icon="item.icon"
              :icon-color="item.iconColor"
              :color="item.color"
              :to="item.to"
            />
          </v-col>
        </template>
      </v-row>
    </div>

    <!-- Data Dosen -->

    <div class="my-8">
      <AdminDashboardProgressCircular />
    </div>

    <v-row>
      <!-- Dosen Elektronika -->
      <v-col cols="6">
        <AdminDashboardProgressLinear />
      </v-col>

      <!-- Jenjang Pendidikan -->
      <v-col cols="6">
       <AdminDashboardBarChart />
      </v-col>
    </v-row>

    <!-- Table -->
  </v-container>
</template>

<script>
export default {
  name: 'AdminDashboard',
  layout: 'admin/default',
  data() {
    return {
      totalData: [
        {
          name: 'Penelitian',
          totalData: 90,
          icon: 'mdi-domain',
          iconColor: 'grey',
          color: 'light-blue darken-4',
          to: '/admin/dashboard'
        },
        {
          name: 'Pengabdian',
          totalData: 90,
          icon: 'mdi-domain',
          iconColor: 'grey',
          color: 'red',
          to: '/admin/dashboard'
        },
        {
          name: 'Sertifikasi',
          totalData: 90,
          icon: 'mdi-domain',
          iconColor: 'grey',
          color: 'yellow',
          to: '/admin/dashboard'
        },
        {
          name: 'Mata Kuliah',
          totalData: 90,
          icon: 'mdi-domain',
          iconColor: 'grey',
          color: 'green',
          to: '/admin/dashboard'
        }
      ]
    }
  }
}
</script>
