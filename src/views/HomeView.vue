<template>
<NavBar/>
<Estudios/>
<FooterVue/>
</template>

<script>
// @ is an alias to /src
import NavBar from '../components/NavBar.vue'
import Estudios from '@/components/Estudios.vue';
import FooterVue from '@/components/Footer.vue';
export default {
  name: 'HomeView',
  components: {
    NavBar,
    Estudios,
    FooterVue
  }
}
</script>
