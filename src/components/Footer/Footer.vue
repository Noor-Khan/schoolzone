<template>
  <section id="footer">
    <div class="large-footer">
      <v-container>
        <v-row>
          <v-col cols="12" md="3" class="text-left">
            <div class="information footer-col">
              <h4>Information</h4>
              <ul>
                <li>
                  <router-link to="/get-access">Contact</router-link>
                </li>
                <li>
                  <a href="#">Jobs</a>
                </li>
                <li>
                  <a href="#">Features</a>
                </li>
                <li>
                  <a href="#">Terms</a>
                </li>
              </ul>
            </div>
          </v-col>
          <v-col cols="12" md="2" class="text-left">
            <div class="student-help footer-col">
              <h4>Student Help</h4>
              <ul>
                <li>
                  <a href="#">FAQ</a>
                </li>
                <li>
                  <a href="#">Privacy</a>
                </li>
              </ul>
            </div>
          </v-col>
          <v-col cols="12" md="4" class="text-left">
            <div class="newsletter footer-col">
              <h4>Newsletter</h4>
              <p>Get latest update, news & academic offers</p>
              <input type="email" placeholder="Subscribe!" />
              <v-btn small color="primary">Subscribe</v-btn>
            </div>
          </v-col>
          <v-col cols="12" md="3" class="text-left">
            <div class="contact footer-col">
              <h4>Contact</h4>
              <ul>
                <li>Headquarters</li>
                <li>ChinesPod LLC</li>
                <li>246 West Broadway, 4th Floor</li>
                <li>New York, NY 10013</li>
                <li>Phone: (+1) 212-666-8000</li>
              </ul>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="bottom-footer">
      <v-container>
        <v-row>
          <v-col cols="12" md="12">
            <p>
              <a href="https://chinesepod.com" target="_blank">ChinesePod</a> - All copyrights reserved © 2020
            </p>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </section>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
#footer {
  background-color: #070707;
  padding-top: 50px;
  .large-footer {
    padding-bottom: 50px;
  }
  .bottom-footer {
    background-color: #000;
    p {
      color: #fff;
      margin-bottom: 0;
    }
  }
  .container {
    max-width: 1400px;
  }
  .footer-col {
    color: #fff;
    padding-right: 20px;
    padding-bottom: 20px;
    a {
      color: #fff;
      letter-spacing: 0.6px;
      &:hover {
        color: #cc433b;
      }
    }
    p {
      letter-spacing: 0.6px;
    }
    input {
      border: 1px solid #efefef;
      height: 45px;
      border-radius: 30px;
      padding: 0px 20px;
      width: 100%;
      font-size: 14px;
      border: 1px solid #cc433b;
      &:focus {
        outline: none;
      }
      &::placeholder {
        color: #fff;
      }
    }
    .v-btn {
      float: right;
      padding: 13px 30px;
      height: unset;
      border-radius: 30px;
      border: 1px solid #cc433b;
      margin-top: -45px;
    }
    h4 {
      margin-bottom: 20px;
      font-family: "Oswald";
      letter-spacing: 1px;
    }
    ul {
      list-style-type: none;
      padding-left: 0;
      li {
        line-height: 36px;
      }
    }
  }
}
</style>