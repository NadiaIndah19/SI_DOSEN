<template>
  <v-container  class="py-6 my-4">
    <v-card
    class="mx-auto"
    max-width="344"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
        <div class="text-overline mb-4">
          OVERLINE
        </div>
        <v-list-item-title class="text-h5 mb-1">
          Headline 5
        </v-list-item-title>
        <v-list-item-subtitle>Greyhound divisely hello coldly fonwderfully</v-list-item-subtitle>
      </v-list-item-content>

      <v-list-item-avatar
        tile
        size="80"
        color="grey"
      ></v-list-item-avatar>
    </v-list-item>

    <v-card-actions>
      <v-btn
        outlined
        rounded
        text
      >
        Button
      </v-btn>
    </v-card-actions>
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