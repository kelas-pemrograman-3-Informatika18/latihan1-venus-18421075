<template>
  <q-page class="bg-cyan-8">
    <div class="row">
      <q-card class="fixed-center col-md-3 col-xs-12 bg-grey-4" flat>
        <q-card-section>
          <div class="text-h5 q-pb-md" align="center">
            Halaman Register
          </div>
          <q-form
            @submit="onSubmit"
            @reset="onReset"
            class="q-gutter-md"
          >
            <q-input
              filled
              v-model="username"
              label="Username"
              lazy-rules
              :rules="[ val => val && val.length > 0 || 'Tolong Ketik Username']"
            />

            <q-input
              filled
              v-model="programStudi"
              label="program studi"
              lazy-rules
              :rules="[ val => val && val.length > 0 || 'Tolong Isi Program Studi']"
            />

            <q-input
              filled
              v-model="namalengkap"
              label="Nama Lengkap"
              lazy-rules
              :rules="[ val => val && val.length > 0 || 'Tolong Isi Nama Lengkap Anda']"
            />

            <q-input
              filled
              type="password"
              v-model="password"
              label="Password"
              lazy-rules
              :rules="[
                val => val !== null && val.length > 0 || 'Password Tidak Boleh Kosong'
              ]"
            />

            <div class="q-gutter-md">
              <q-btn label="Register" type="submit" color="primary"/>
              <q-btn label="Login"  to="/" flat color="primary"/>
            </div>
        </q-form>
        </q-card-section>
    </q-card>
    </div>
  </q-page>
</template>
<script>
export default {
  data () {
    return {
      username: null,
      password: null,
      programStudi: null,
      namalengkap: null
    }
  },
  methods: {
    onSubmit () {
    },
    onReset () {
      this.username = null
      this.password = null
    }
  }
}
</script>
