<template>
  <div class="container">
    <cv-satu />
  <br><br><br><br><br>
    <cv-dua />
  </div>
</template>

<script>
import CvSatu from './components/CvSatu.vue'
import CvDua from './components/CvDua.vue'

export default {
  name: 'App',
  components: {
    CvSatu,
    CvDua
  }
}
</script>

<style>

</style>
