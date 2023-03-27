<script>
import AppNavbar from "./components/AppNavbar.vue";
import AppMain from "./components/AppMain.vue";
import AppHeader from "./components/AppHeader.vue";
import AppSection from "./components/AppSection.vue";
import AppFooter from "./components/AppFooter.vue";



export default {
  data() {
    return {};
  },

  components: {
    AppNavbar,
    AppMain,
    AppHeader,
    AppSection,
    AppFooter,
  }

}


</script>

<template>
  <AppNavbar></AppNavbar>
  <AppMain></AppMain>
  <AppHeader></AppHeader>
  <AppSection></AppSection>
  <AppFooter></AppFooter>
</template>

<style lang="scss" scoped>
template {
  height: 100vh;
  width: 100vw;
}
</style>