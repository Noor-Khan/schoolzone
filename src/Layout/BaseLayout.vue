<template>
  <div>
    <navbar />
    <v-content>
      <div class="base-layout">
        <router-view />
      </div>
    </v-content>
    <Footer />
  </div>
</template>
<script>
import Navbar from "../components/Navigation/Navbar";
import Footer from "../components/Footer/Footer";
export default {
  components: {
    Navbar,
    Footer
  }
};
</script>
<style lang="scss" scoped>
.base-layout {
  position: relative;
}
</style>