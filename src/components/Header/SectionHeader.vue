<template>
  <div class="section-header">
    <div class="header-overlay"></div>
    <v-row>
      <v-col cols="12" md="12">
        <div class="header-logo">
          <img src="../../assets/images/logo-mini.png" alt class="img-fluid" />
        </div>
      </v-col>
    </v-row>
  </div>
</template>
<style lang="scss" scoped>
.section-header {
  position: relative;
  display: flex;
  align-items: center;
  background-image: url("../../assets/images/header-bg2.jpg");
  background-size: 140%;
  background-position: center center;
  background-attachment: fixed;
  height: 400px;
  .header-overlay {
    position: absolute;
    width: 100%;
    height: 100%;
    left: 0;
    top: 0;
    background-color: rgba(41, 41, 41, 0.9019607843137255);
  }
  .header-logo {
    position: relative;
  }
  &:after {
    content: "";
    position: absolute;
    width: 50px;
    background: white;
    height: 50px;
    right: 0;
    left: 0;
    bottom: -25px;
    transform: rotate(45deg);
    text-align: center;
    margin: auto;
  }
}
</style>