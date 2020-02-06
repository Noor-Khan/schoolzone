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
          icon: "images/icons/calendar.png",
          heading: "Years of experience",
          para:
            "ChinesePod podcasts and videos are recorded by native Chinese teachers with years of teaching Chinese as a second language."
        },
        {
          icon: "images/icons/multi-device.png",
          heading: "Multi device",
          para:
            "The platform is responsive to any device and Operating System to provide a stable and engaging experience across platforms."
        },
        {
          icon: "images/icons/audio.png",
          heading: "Audo lessions",
          para:
            "An integrated player in the SchoolZone main page lets students have a quick preview of the most recent lesson posted by their teacher."
        },
        {
          icon: "images/icons/video.png",
          heading: "Video Lessons",
          para:
            "All the Video Content from ChinesePod are easily accessible for students and teachers using the platform."
        },
        {
          icon: "images/icons/support.png",
          heading: "Dedicated support",
          para:
            "Students and teachers using the platform will have special dedicated support staff to solve any questions or technical issues when they email schoolzone[at]chinesepod.com"
        }
      ]
    };
  }
};
</script>
<style lang="scss" scoped>
#features {
  padding: 50px 0;
  .container {
    max-width: 1400px;
  }
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
    height: 42vh;
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