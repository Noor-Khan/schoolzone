<template>
  <v-btn
    v-if="btnClass === 'access'"
    :href="link"
    :color="btnClass"
    :rounded="true"
    class="px-6 py-6"
    :class="`btn-${btnClass}`"
    style="text-decoration:none;"
  >{{ text }}</v-btn>
  <v-btn
    :disabled="disabled"
    v-else
    :href="link"
    :color="btnClass"
    :rounded="true"
    class="px-12 py-7"
    :class="`btn-${btnClass}`"
    style="text-decoration:none;"
  >{{ text }}</v-btn>
</template>
<script>
export default {
  props: {
    text: {
      type: String,
      required: true
    },
    link: {
      type: String,
      default: "##"
    },
    btnClass: {
      type: String,
      default: "#5733FF"
    },
    disabled: {
      type: Boolean,
      default: false
    }
  }
};
</script>
<style lang="scss" scoped>
.btn-access {
  font-size: 14px !important;
  background-color: #00b233 !important;
  color: #fff !important;
  font-weight: 600;
  text-transform: capitalize;
  border: 1px solid #00b233;
  &:hover {
    background-color: #fff !important;
    color: #00b233 !important;
    border: 1px solid #00b233;
  }
}
</style>