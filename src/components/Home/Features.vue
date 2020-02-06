<template>
  <section id="features">
    <v-container>
      <v-row class="mb-10">
        <v-col cols="12" md="10" offset-md="1">
          <div class="main-heading text-uppercase">
            <h2>how to use chinespod schoolzone</h2>
          </div>
          <div class="main-para">
            <p>When used in combination with a specific curriculum, ChinesePod SchoolZone can be used as part of the classroom activities, for listening practice or further cultural insights about a certain topic of modern Chinese society.</p>
          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" md="4" v-for="(service, index) in services" :key="index">
          <div class="feature one">
            <div class="icon">
              <img :src="service.icon" alt />
            </div>
            <div class="heading">
              <h4>{{service.heading}}</h4>
            </div>
            <hr class="seperator" />
            <div class="para">
              <p>{{service.para}}</p>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
export default {
  data() {
    return {
      services: [
        {
          icon: "images/icons/engage.png",
          heading: "Engaging activities",
          para:
            "ChinesePod SchoolZone can be used by students to help them go over topics addressed in class as well as expand explanations about a particular grammar point."
        },
        {
          icon: "images/icons/engage.png",
          heading: "Years of experience",
          para:
            "ChinesePod SchoolZone can be used by students to help them go over topics addressed in class as well as expand explanations about a particular grammar point."
        },
        {
          icon: "images/icons/engage.png",
          heading: "Multi device",
          para:
            "ChinesePod SchoolZone can be used by students to help them go over topics addressed in class as well as expand explanations about a particular grammar point."
        },
        {
          icon: "images/icons/engage.png",
          heading: "Audo lessions",
          para:
            "ChinesePod SchoolZone can be used by students to help them go over topics addressed in class as well as expand explanations about a particular grammar point."
        },
        {
          icon: "images/icons/engage.png",
          heading: "Video Lessons",
          para:
            "ChinesePod SchoolZone can be used by students to help them go over topics addressed in class as well as expand explanations about a particular grammar point."
        },
        {
          icon: "images/icons/engage.png",
          heading: "Dedicated support",
          para:
            "ChinesePod SchoolZone can be used by students to help them go over topics addressed in class as well as expand explanations about a particular grammar point."
        }
      ]
    };
  }
};
</script>
<style lang="scss" scoped>
#features {
  padding: 50px 0;
  .main-heading {
    h2 {
      font-size: 36px;
    }
  }
  .feature {
    background-color: #efefef;
    padding: 10px 15px;
    margin-top: 50px;
    box-shadow: 0px 0px 15px 0px #f0f0f0;
    .icon {
      position: relative;
      top: -55px;
      background-color: #efefef;
      box-shadow: 0px 0px 0px 5px #fff;
      width: 100px;
      height: 100px;
      line-height: 100px;
      border-radius: 50%;
      margin: 0 auto;
      padding: 20px;
      img {
        align-items: center;
        width: 60px;
        display: inline;
      }
    }
    .heading {
      margin: 10px 0;
    }
    .seperator {
      width: 100px;
      margin: auto;
      border-color: #cc433b;
    }
    .para {
      margin: 10px 0;
      p {
        line-height: 26px;
      }
    }
  }
}
</style>