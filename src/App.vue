<script setup>
import { ref, onMounted} from 'vue';
import SeriesList from './components/SeriesList.vue';
import Navbar from './components/Navbar.vue';

let webSeriesRes = ref([]);
 onMounted(() => {
  fetch('https://karthikborra-web-series-nodejs.onrender.com/api')
    .then(response => response.json())
   .then(res => webSeriesRes.value = res)
});


      
 
</script>

<template>
  <header>
      <Navbar />
  </header>

  <main>
   <div class="container">
      <SeriesList :seriesList="webSeriesRes" />
   </div>
  </main>
</template>

<style scoped>

</style>
