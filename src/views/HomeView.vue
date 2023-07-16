<template>
<NavBar/>
<Estudios/>
</template>

<script>
// @ is an alias to /src
import NavBar from '../components/NavBar.vue'
import Estudios from '@/components/Estudios.vue';
export default {
  name: 'HomeView',
  components: {
    NavBar,
    Estudios
  }
}
</script>
