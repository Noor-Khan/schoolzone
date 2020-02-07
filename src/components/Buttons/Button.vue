<template>
  <v-btn
    v-if="btnClass === 'access'"
    color="success"
    :rounded="true"
    :to="link"
    class="px-8 py-4"
    :class="`btn-${btnClass}`"
    style="text-decoration:none;"
  >{{ text }}</v-btn>
  <v-btn
    v-else
    :href="link"
    color="success"
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
<style lang="scss">
.btn-access {
  font-size: 14px !important;
  color: #fff !important;
  font-weight: 600;
  width: 180px;
  height: unset !important;
  text-transform: capitalize;
  &:hover {
    background-color: transparent !important;
    color: #fff !important;
  }
}
.btn-submit {
  border-radius: 30px;
  padding: 16px 40px;
  margin: 5px;
  font-size: 16px;
  height: unset;
}
</style>