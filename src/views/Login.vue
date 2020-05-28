<template>
  <section id="login">
    <section-header />
    <v-container>
      <v-row>
        <v-col cols="12" md="8" offset-md="2">
          <div class="login-form">
            <v-form ref="form" v-model="valid">
              <h3>Login</h3>
              <hr class="seperator" />
              <v-text-field
                v-model="email"
                prepend-icon="mdi-email-open"
                :rules="emailRules"
                label="Email"
                required
              ></v-text-field>
              <v-text-field
                v-model="password"
                type="password"
                prepend-icon="mdi-key"
                :rules="rules"
                label="Password"
                required
              ></v-text-field>
              <div class="d-flex just" style="justify-content: space-between;">
                <v-checkbox v-model="checkbox" label="Remember me?" required></v-checkbox>
                <div class="forgot-password">
                  <a href="#">Forgot password?</a>
                </div>
              </div>
              <submit-button text="Log in" btnClass="submit" @click.native="submit()" />
            </v-form>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
import SectionHeader from "../components/Header/SectionHeader";
import SubmitButton from "../components/Buttons/Button";
export default {
  components: {
    SectionHeader,
    SubmitButton
  },
  data() {
    return {
      email: "",
      password: "",
      rules: [v => !!v || "Password is required"],
      emailRules: [
        v => !!v || "E-mail is required",
        v => /.+@.+\..+/.test(v) || "E-mail must be valid"
      ]
    };
  },
  methods: {
    submit() {
      if (this.$refs.form.validate()) {
        alert("submitted!");
      }
    }
  }
};
</script>
<style lang="scss" scoped>
#login {
  padding: 50px 0;
  .login-form {
    background-color: #fbfbfb;
    margin: 20px 10px;
    padding: 30px 40px;
    border-radius: 10px;
    h3 {
      font-size: 32px;
      text-transform: uppercase;
    }
    .seperator {
      width: 50px;
      margin: 10px auto;
      border: 1px solid #cc433b;
    }
    .forgot-password {
      margin-top: 20px;
    }
  }
}
</style>