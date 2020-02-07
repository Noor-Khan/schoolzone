<template>
  <section id="homeSlider">
    <template>
      <v-carousel hide-delimiters height="100vh">
        <v-carousel-item v-for="(slide,i) in slides" :key="i" :src="slide.src">
          <v-container class="align-center d-flex">
            <v-row class>
              <v-col cols="12" md="10" lg="10" xl="6" offset-xl="1">
                <div class="slide-content px-5 text-left">
                  <div class="slide-upper-heading">
                    <h4>{{slide.upperHeading}}</h4>
                  </div>
                  <hr class="seperator" />
                  <div class="slide-main-heading">
                    <h2>{{slide.mainHeading}}</h2>
                  </div>
                  <div class="slide-para">
                    <p>{{slide.para}}</p>
                  </div>
                </div>
              </v-col>
            </v-row>
          </v-container>
        </v-carousel-item>
      </v-carousel>
    </template>
  </section>
</template>
<script>
export default {
  data() {
    return {
      slides: [
        {
          src: "images/schoolzone-lerning.jpg",
          upperHeading: "Welcome to ChinesPod SchoolZone",
          mainHeading: "A New Way to Teach and Learn",
          para:
            "ChinesePod SchoolZone offers a meeting place for teachers and students to immerse into ChinesePod content and move their Chinese learning to the next level. With the combination of a classroom experience, the possibilities for learning are limitless."
        },
        {
          src: "images/student-of-schoolzone.jpg",
          upperHeading: "The Best Learning Tools in the Classroom",
          mainHeading: "Technology for Learning",
          para:
            "With extensive content and a practical set of learning tools included in each lesson, institutions using ChinesePod SchoolZone can impact the engagement of the students in their Chinese learning process and attract more students to their programs."
        },
        {
          src: "images/schoolzone.jpg",
          upperHeading: "Learn Anywhere",
          mainHeading: "Mobile-Ready",
          para:
            "ChinesePod SchoolZone platform has been created to consider every device. Its responsive design lets you access all the classroom content on the go, so students and teachers can focus on their lessons anytime, anywhere."
        }
      ]
    };
  }
};
</script>
<style lang="scss">
#homeSlider {
  .slide-content {
    color: #fff;
    .slide-upper-heading {
      h4 {
        font-weight: 300;
      }
    }
    .slide-main-heading {
      h2 {
        font-size: 50px;
        font-weight: 700;
      }
    }
    .slide-para {
      p {
        font-size: 18px;
        letter-spacing: 0.5px;
        line-height: 28px;
      }
    }
    .seperator {
      width: 50px;
      margin: 10px 0;
      border: 1px solid #cc433b;
    }
  }
}

// Slider Styling
.v-image__image--cover {
  background-attachment: fixed;
}
#homeSlider {
  .v-responsive__content {
    display: flex !important;
    background-color: rgba(0, 0, 0, 0.44);
    &:after {
      content: "";
      position: absolute;
      background: white;
      width: 150px;
      height: 150px;
      right: 0;
      left: 0;
      bottom: -5rem;
      transform: rotate(45deg);
      text-align: center;
      margin: auto;
      @media (max-width: 580px) {
        width: 100px;
        height: 100px;
      }
    }
  }
}
.v-window__prev,
.v-window__next {
  margin: 0 20px;
  transform: rotate(45deg);
  border-radius: 0;
  @media (max-width: 580px) {
    top: unset !important;
    bottom: calc(10% - 20px);
  }
  button {
    transform: rotate(-45deg);
    width: 60px !important;
    height: 60px !important;
    @media (max-width: 580px) {
      width: 45px !important;
      height: 45px !important;
    }
    span {
      i {
        font-size: 36px !important;
      }
    }
  }
}
</style>