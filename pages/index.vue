<template>
  <v-container class="pa-0 ma-0" fluid>
    <v-row class="home pa-0 ma-0" justify="center" align-content="center">
      <logo />
      <h2 class="home__subtitle">Creamos experiencias en la web</h2>
      <a class="mail" href="mailto:hola@enalbis.com">hola@enalbis.com</a>
    </v-row>
  </v-container>
</template>

<script>
import Logo from '@/components/Logo'
export default {
  components: {
    Logo,
  },
}
</script>

<style scoped lang="scss">
.home {
  position: relative;
  flex-direction: column;
  background-color: $enalbis-aqua;
  height: 100vh;
  &__subtitle {
    color: white;
    margin-left: 1rem;
    margin-top: 1rem;
  }
}
.mail {
  position: absolute;
  color: white;
  text-decoration: none;
  bottom: 7rem;
  left: -3rem;
  transform: rotate(-90deg);
  font-size: 1.5rem;
}
</style>
