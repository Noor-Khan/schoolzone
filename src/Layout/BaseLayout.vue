<template>
  <div>
    <navbar />
    <v-content>
      <div class="base-layout">
        <router-view />
      </div>
    </v-content>
  </div>
</template>
<script>
import Navbar from "../components/Navigation/Navbar";
export default {
  components: {
    Navbar
  }
};
</script>
<style lang="scss" scoped>
.base-layout {
  position: relative;
}
</style>