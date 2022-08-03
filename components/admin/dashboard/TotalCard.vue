<template>
  <div>
    <base-card size="s" :color="color">
      <v-row justify="space-between">
        <v-col cols="6">
          <v-card-title class="py-3 px-3 white--text font-weight-bold"
            >{{ totalData }}
          </v-card-title>
          <v-card-subtitle class="py-3 px-3 white--text font-weight-bold"
            >{{ name }}
          </v-card-subtitle>
        </v-col>
        <v-col class="d-flex justify-center align-center">
          <v-icon size="64" :color="iconColor"> {{ icon }} </v-icon>
        </v-col>
      </v-row>
      <div class="d-flex justify-center align-center">
        <v-btn nuxt to="to" plain class="white--text"
          >More Info <v-icon right> mdi-arrow-right-bold-circle </v-icon></v-btn
        >
      </div>
    </base-card>
  </div>
</template>

<script>
export default {
  name: 'DashboardTotalCard',
  props: {
    totalData: {
      type: [String, Number],
      required: true,
      default: 80
    },
    name: {
      type: String,
      required: true,
      default: 'peraturan'
    },
    icon: {
      type: String,
      required: true,
      default: 'mdi-domain'
    },
    iconColor: {
      type: String,
      default: 'grey'
    },
    color: {
      type: String,
      required: true,
      default: 'light-blue darken-4'
    },
    to: {
      type: String,
      required: true,
      default: '/admin/dashboard'
    }
  }
}
</script>
