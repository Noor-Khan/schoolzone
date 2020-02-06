<template>
  <div id="Home">
    <slider />
    <services />
    <counters />
    <features />
  </div>
</template>

<script>
import Slider from "../components/Home/Slider";
import Services from "../components/Home/Services";
import Counters from "../components/Home/Counters";
import Features from "../components/Home/Features";
export default {
  components: {
    Slider,
    Services,
    Counters,
    Features
  }
};
</script>
