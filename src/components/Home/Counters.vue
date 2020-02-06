<template>
  <section id="counters">
    <div class="counter-overlay"></div>
    <v-container>
      <v-row>
        <v-col cols="12" md="3" v-for="(count, index) in counters" :key="index">
          <div class="counter one">
            <div class="icon">
              <img :src="count.icon" alt />
            </div>
            <div class="counts">
              <ICountUp
                :delay="delay"
                :endVal="count.counts"
                :options="options"
                @ready="onReady(count.counts)"
              />
            </div>
            <div class="heading text-uppercase">
              <h4>{{count.heading}}</h4>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
import ICountUp from "vue-countup-v2";
export default {
  components: {
    ICountUp
  },
  data() {
    return {
      counters: [
        { icon: "images/icons/books.png", counts: 3650, heading: "lessons" },
        { icon: "images/icons/students.png", counts: 578, heading: "students" },
        { icon: "images/icons/schools.png", counts: 223, heading: "schools" },
        { icon: "images/icons/teachers.png", counts: 60, heading: "teachers" }
      ],
      delay: 3000,
      duration: 5000,
      // endVal: 3650,
      options: {
        useEasing: true,
        useGrouping: true,
        separator: "",
        decimal: ".",
        prefix: "",
        suffix: ""
      }
    };
  },
  methods: {
    onReady(instance, endVal) {
      // const that = this;
      instance.update(endVal + 100);
    }
  }
};
</script>
<style lang="scss" scoped>
#counters {
  background-image: url("../../assets/images/child.jpg");
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  padding: 50px 0;
  .counter {
    color: #fff;
    .icon {
      img {
        width: 90px;
      }
    }
    .counts {
      span {
        font-size: 42px;
        font-weight: 600;
      }
    }
    .heading {
      h4 {
        font-size: 22px;
        font-weight: 400;
      }
    }
  }
  .counter-overlay {
    background-color: #000;
    width: 100%;
    height: 100%;
  }
}
</style>