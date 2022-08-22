<template>
  <v-app dark>
    <NavBar />
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import NavBar from '~/components/NavBar.vue'
import Footer from '~/components/Footer.vue'
export default {
  name: 'DefaultLayout',
  data() {
    return {}
  },
  components: { NavBar, Footer, Footer },
}
</script>
