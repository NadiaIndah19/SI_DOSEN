<template>
  <v-container  class="py-6 my-4">
    <v-card light>
    <v-card-title>
      Penelitian Dosen
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
            text: 'Nama Dosen',
            align: 'start',
            sortable: false,
            value: 'name',
          },
          { text: 'Judul Penelitian', value: 'judul' },
          { text: 'Keyword', value: 'keyword' },
        //   { text: 'Tanggal Pelaksanaan', value: 'tgl_pelaksanaan' },
        //   { text: 'SK Kontrak', value: 'sk' },
          {text: 'Action', value: 'action'}
        ],
        desserts: [
          {
            name: 'Desy Intan Permatasari',
            judul: 'Pengembangan Model Rekomendasi UX Melalui Pendekatan Agile untuk Produk Virtual Exhibition',
            keyword: 'Virtual Exhibition',
            // tgl_pelaksanaan: '12-10-2016',
            // sk: 'uploads/sk-kontrak/20210823143917-2021-Penetapan Judul Penelitian Lokal.pdf',
          },
          {
            name: 'Fitri Setyorini',
            judul: 'Pengembangan Model Rekomendasi UX Melalui Pendekatan Lean Startup untuk Produk Virtual Exhibition',
            keyword: 'Virtual Exhibition, Pandemi Covid 19',
            // tgl_pelaksanaan: '19-02-2018',
            // sk: 'uploads/sk-kontrak/20210823143917-2021-Penetapan Judul Penelitian Lokal.pdf',
          },
          {
            name: 'Zainal Arief',
            judul: 'Pengembangan Model Rekomendasi UX Melalui Pendekatan UX Research',
            keyword: 'OrionsPro, UX research',
            // tgl_pelaksanaan: '20-05-2020',
            // sk: 'uploads/sk-kontrak/20210823143917-2021-Penetapan Judul Penelitian Lokal.pdf',
          },
          {
            name: 'Andhik Ampuh Yunanto',
            judul: 'Pengembangan Model Rekomendasi UX Melalui Pendekatan UX Research, Agile, dan Lean Startup untuk Produk Virtual Exhibition',
            keyword: 'UX research',
            // tgl_pelaksanaan: '08-11-2019',
            // sk: 'uploads/sk-kontrak/20210823143917-2021-Penetapan Judul Penelitian Lokal.pdf',
          },
        ],
      }
    },
     layout: 'admin/default',
  }
</script>