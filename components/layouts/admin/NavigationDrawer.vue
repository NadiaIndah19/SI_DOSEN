<template>
  <v-navigation-drawer
    :value="drawer"
    app
    color="indigo darken-1"
    mobile-breakpoint="960"
    temporary
    width="260"
    @input="(payload) => UPDATE_DRAWER(payload)"
  >
    <template v-if="drawerImage" #img="props">
      <v-img :key="image" v-bind="props" />
    </template>
    <div class="px-2">
      <AdminLayoutHeaderDrawer />

      <v-divider class="mx-3 mb-2" />

      <AdminLayoutList :items="items" />
    </div>
  </v-navigation-drawer>
</template>

<script>
import { mapState, mapMutations } from 'vuex'

export default {
  name: 'AdminNavigationDrawer',
  data() {
    return {
      navigationDrawer: this.drawer,
      drawerImage: false,
      mini: true,
      items: [
        // {
        //   title: 'Dashboard',
        //   icon: 'mdi-view-dashboard',
        //   to: '/admin/dashboard'
        // },
        {
          title: 'Dashboard',
          icon: 'mdi-view-dashboard',
          to: '/admin/dashboard'
        },
        {
          title: 'Profil Dosen',
          icon: 'mdi-account-group',
          to: '/admin/dosen'
        },
        {
          title: 'Penelitian',
          icon: 'mdi-magnify',
          to: '/admin/penelitian'
        },
        {
          title: 'Pengabdian',
          icon: 'mdi-book-multiple',
          to: '/admin/pengabdian'
        },
        {
          title: 'Sertifikasi',
          icon: 'mdi-note-text-outline',
          to: '/admin/sertifikasi'
        },
        {
          title: 'Mata Kuliah',
          icon: 'mdi-human-male-board',
          to: '/admin/matakuliah'
        }
      ]
    }
  },
  computed: {
    ...mapState('ui/admin', {
      drawer: 'drawer'
    })
  },
  methods: {
    ...mapMutations('ui/admin', {
      UPDATE_DRAWER: 'UPDATE_DRAWER'
    })
  }
}
</script>
