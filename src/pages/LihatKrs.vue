<template>
    <q-page padding>
          <div class="q-pa-md">
    <q-table
      title="KRS"
      :data="data"
      :columns="columns"
      row-key="name"
    />
  </div>
</q-page>
</template>
<script>
export default {
  data () {
    return {
      columns: [
        {
          name: 'name',
          required: true,
          label: 'No',
          align: 'left',
          field: row => row.name,
          format: val => `${val}`,
          sortable: true
        },
        { name: 'kodematakuliah', align: 'center', label: 'Kode Mata Kuliah', field: 'kodematakuliah', sortable: true },
        { name: 'namamatakuliah', align: 'center', label: 'Nama Mata Kuliah', field: 'namamatakuliah', sortable: true },
        { name: 'kelas', align: 'center', label: 'Kelas', field: 'kelas' },
        { name: 'sks', align: 'center', label: 'SKS', field: 'sks' },
        { name: 'hari', align: 'center', label: 'Hari', field: 'hari' },
        { name: 'namadosen', align: 'center', label: 'Nama Dosen', field: 'namadosen', sortable: true },
        { name: 'parafujian', align: 'center', label: 'Paraf Ujian', field: 'parafujian', sortable: true }
      ],
      data: [
        {
          name: '1',
          kodematakuliah: 'FK405',
          namamatakuliah: 'iNTERAKSI MANUSIA DAN KOMPUTER',
          kelas: '04',
          sks: '3',
          hari: 'SENIN',
          namadosen: 'AHMAD CUCUS',
          parafujian: ''
        },
        {
          name: '2',
          kodematakuliah: 'FK403',
          namamatakuliah: 'SISTEM OPERASI',
          kelas: '03',
          sks: '3',
          hari: 'SELASA',
          namadosen: 'ARNES YULI VANDIKA',
          parafujian: ''
        },
        {
          name: '3',
          kodematakuliah: 'UN402',
          namamatakuliah: 'ENTREPREUNERSHIP(INCUBATOR CLASS',
          kelas: '15',
          sks: '2',
          hari: 'SELASA',
          namadosen: 'FENTY ARIANI',
          parafujian: ''
        },
        {
          name: '4',
          kodematakuliah: 'IF603',
          namamatakuliah: 'SISTEM KEAMANAN KOMPUTER',
          kelas: '03',
          sks: '3',
          hari: 'RABU',
          namadosen: 'ADI WIJAYA',
          parafujian: ''
        },
        {
          name: '5',
          kodematakuliah: 'FK404',
          namamatakuliah: 'DATA MINING',
          kelas: '04',
          sks: '3',
          hari: 'RABU',
          namadosen: 'IING LUKMAN',
          parafujian: ''
        },
        {
          name: '6',
          kodematakuliah: 'FK402',
          namamatakuliah: 'TEORI BAHASA FORMAL DAN OTOMATA',
          kelas: '01',
          sks: '3',
          hari: 'KAMIS',
          namadosen: 'WAMILIANA',
          parafujian: ''
        },
        {
          name: '7',
          kodematakuliah: 'FK401',
          namamatakuliah: 'PEMROGAMAN III',
          kelas: '04',
          sks: '3',
          hari: 'KAMIS',
          namadosen: 'DIKA HASTANTO',
          parafujian: ''
        },
        {
          name: '8',
          kodematakuliah: 'FK402',
          namamatakuliah: 'PRAK.PEMROGAMAN III',
          kelas: '04',
          sks: '1',
          hari: 'KAMIS',
          namadosen: 'TAQWAN',
          parafujian: ''
        },
        {
          name: '9',
          kodematakuliah: 'FK206',
          namamatakuliah: 'ANALISA KEBUTUHAN SISTEM',
          kelas: '06',
          sks: '3',
          hari: 'JUMAT',
          namadosen: 'YUTSI APRILINDA',
          parafujian: ''
        }
      ]
    }
  }
}
</script>
