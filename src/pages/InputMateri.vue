<template>
    <q-page padding>
        <q-card flat class="bg-grey-2">
            <q-card-section>
                <div class="text-h7">Input Materi</div>
                <q-form
                    @submit="onSubmit"
                    @reset="onReset"
                    class="q-gutter-md"
                >
                    <div class="q-gutter-md">
                    <q-input label="Judul Materi" v-model="judul" filled :rules="[ val => val && val.length > 0 || 'Harap Masukan Judul']"></q-input>
                    <q-input label="Hari" v-model="hari"  filled :rules="[ val => val && val.length > 0 || 'Harap Masukan Hari']"></q-input>
                    <q-input label="Waktu" v-model="waktu"  filled :rules="[ val => val && val.length > 0 || 'Harap Masukan Waktu']"></q-input>
                    <q-btn type="submit" label="Input" color="teal" unelevated></q-btn>
                    <q-btn type="reset" label="Reset" color="teal" flat unelevated></q-btn>
                    </div>
                </q-form>
            </q-card-section>
        </q-card>
    </q-page>
</template>
<script>
export default {
  data () {
    return {
      judul: null,
      hari: null,
      waktu: null
    }
  },
  methods: {
    onReset () {
      this.judul = null
      this.hari = null
      this.waktu = null
    },
    onSubmit () {
      this.$q.notify({
        type: 'positive',
        message: 'Berhasil Input Materi'
      })
      this.$router.push({ name: 'dashboard' })
    }
  }
}
</script>
