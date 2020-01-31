<template>
  <div>
    <v-content>
      <div class="base-layout">
        <router-view />
      </div>
    </v-content>
  </div>
</template>
<script>
export default {
  components: {}
};
</script>
<style lang="scss" scoped>
.base-layout {
  position: relative;
}
</style>