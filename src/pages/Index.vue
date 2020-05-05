<template>
  <q-page padding>
  <div class="q-pa-md">
    <q-carousel
      animated
      v-model="slide"
      arrows
      navigation
      infinite
      autoplay
      transition-prev="slide-right"
      transition-next="slide-left"
      height="550px"
      widht="370px"
    >
      <q-carousel-slide :name="1" img-src="statics/college-students.jpg" />
      <q-carousel-slide :name="2" img-src="statics/mahasiswa-3.jpg" />
    </q-carousel>
  </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      slide: 1
    }
  }
}
</script>
