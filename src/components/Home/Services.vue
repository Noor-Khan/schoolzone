<template>
  <section id="services">
    <v-container>
      <v-row>
        <v-col cols="12" md="4">
          <div class="student service-box text-left">
            <div class="icon">
              <img src="../../assets/icons/book.png" alt />
            </div>
            <div class="heading">
              <h4>Student-Focused</h4>
              <hr class="seperator" />
            </div>
            <div class="para">
              <p>With the use of ChinesePod SchoolZone, students can focus on the lessons that will help them to improve faster according to their level of expertise. Students can bring questions to the classroom and get feedback from their teacher.</p>
            </div>
          </div>
        </v-col>
        <v-col cols="12" md="4">
          <div class="teacher service-box text-left">
            <div class="icon">
              <img src="../../assets/icons/school.png" alt />
            </div>
            <div class="heading">
              <h4>Tech For Teachers</h4>
              <hr class="seperator" />
            </div>
            <div class="para">
              <p>Teachers can save time on lesson preparation and help their students advance by focusing on specific learning challenges. When doing homework or studying for upcoming tests, ChinesePod SchoolZone is a great way to keep students engaged in their learning.</p>
            </div>
          </div>
        </v-col>
        <v-col cols="12" md="4">
          <div class="classroom service-box text-left">
            <div class="icon">
              <img src="../../assets/icons/talk.png" alt />
            </div>
            <div class="heading">
              <h4>Challenging Classrooms</h4>
              <hr class="seperator" />
            </div>
            <div class="para">
              <p>Teachers can easily divide their students between classrooms and levels so it’s easier to give them challenging lessons according to their levels.</p>
            </div>
          </div>
        </v-col>
      </v-row>
      <v-row class="mt-12">
        <v-col cols="12" md="8">
          <div class="video text-left">
            <iframe
              width="100%"
              height="450"
              src="https://www.youtube.com/embed/8tscDj-tXgU"
              frameborder="0"
              allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
        </v-col>
        <v-col cols="12" md="4" class="text-left">
          <div class="video-heading">
            <h3>What is ChinesePod SchoolZone ?</h3>
            <hr class="seperator" />
          </div>
          <div class="video-para">
            <p>
              ChinesePod SchoolZone is a dedicated platform for Students and Teachers to engage around a specific topic and use it as a part of their classroom learning experience.
              When used in combination with a specific curriculum, ChinesePod SchoolZone can be used as part of the classroom activities, for listening practice or further cultural insights about a certain topic of modern Chinese society.
            </p>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
#services {
  position: relative;
  padding: 50px 0;
  z-index: 1;
  .container {
    max-width: 1400px;
  }
  .service-box {
    padding: 30px 20px;
    background-color: #efefef;
    height: 45vh;
    box-shadow: 0px 0px 10px 0px #f6f6f6;
    .icon {
      position: relative;
      margin: 10px 0;
      &:after {
        content: "";
        position: absolute;
        width: 70px;
        height: 70px;
        background-color: red;
        border-radius: 50%;
        left: 30px;
        top: -20px;
        z-index: 20px;
        opacity: 0.3;
      }
      img {
        position: relative;
        z-index: 1;
        width: 70px;
      }
    }
    .heading {
      margin: 10px 0;
      h4 {
        font-size: 22px;
        // font-weight: 600;
        text-transform: uppercase;
      }
      .seperator {
        width: 50px;
        border: 1px solid #cc433b;
      }
    }
    .para {
      p {
        font-size: 16px;
        line-height: 26px;
        letter-spacing: 0.5px;
      }
    }
    &.student {
      .icon {
        &:after {
          background-color: #cf8bfc;
        }
      }
    }
    &.teacher {
      .icon {
        &:after {
          background-color: #40708c;
        }
      }
    }
    &.classroom {
      .icon {
        &:after {
          background-color: #5aba9a;
        }
      }
    }
  }
  .video-heading {
    margin-bottom: 2rem;
    h3 {
      font-size: 42px;
    }
    .seperator {
      width: 50px;
      margin: 10px 0;
      border: 1px solid #cc433b;
    }
  }
  .video-para {
    p {
      line-height: 28px;
      letter-spacing: 0.5px;
    }
  }
}
</style>