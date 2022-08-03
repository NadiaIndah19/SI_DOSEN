<template>
  <v-container  class="py-6 my-4">
    <v-card light>
    <v-card-title>
      Mata Kuliah
      <v-spacer></v-spacer>
      <v-text-field
        v-model="search"
        append-icon="mdi-magnify"
        label="Search"
        single-line
        hide-details
      ></v-text-field>
    </v-card-title>
    <v-data-table
           light
      :headers="headers"
      :items="desserts"
      :search="search"
    >
     <template v-slot:[`item.action`]>
    <v-btn
      tile
      color="success"
      elevation="0"
    >
      <v-icon left>
        mdi-eye
      </v-icon>
      View 
    </v-btn>
    <v-btn
      tile
      color="primary"
      elevation="0"
    >
      <v-icon left>
        mdi-pencil
      </v-icon>
      Edit 
    </v-btn>
    <v-btn
      tile
      color="red"
      elevation="0"
    >
      <v-icon left>
        mdi-delete
      </v-icon>
      Delete 
    </v-btn>
     </template>
    </v-data-table>
    
  </v-card>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        search: '',
        headers: [
          {
            text: 'Nama',
            align: 'start',
            sortable: false,
            value: 'name',
          },
          { text: 'NIP', value: 'nip' },
          { text: 'Gelar Depan', value: 'gelar_dpn' },
          { text: 'Gelar Belakang', value: 'gelar_blk' },
          { text: 'Email', value: 'email' },
          {text: 'Action', value: 'action'}
        ],
        desserts: [
          {
            name: 'Desy Intan Permatasari',
            nip: 198603232015042004n,
            gelar_dpn: ' ',
            gelar_blk: 'S.Kom., M.Kom.',
            email: 'desy@pens.ac.id',
          },
          {
            name: 'Fitri Setyorini',
            nip: 197707072001122001n,
            gelar_dpn: ' ',
            gelar_blk: 'ST., M.Sc',
            email: 'fitri@pens.ac.id',
          },
          {
            name: 'Zainal Arief',
            nip: 196701281990031002n,
            gelar_dpn: 'Dr',
            gelar_blk: 'S.T., M.T.',
            email: 'arief@pens.ac.id',
          },
          {
            name: 'Andhik Ampuh Yunanto',
            nip: 199208022019031013n,
            gelar_dpn: ' ',
            gelar_blk: 'S.Kom., M.Kom.',
            email: 'andhik@pens.ac.id',
          },
        ],
      }
    },
     layout: 'admin/default',
  }
</script>