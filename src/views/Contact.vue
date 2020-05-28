<template>
  <section id="contact">
    <section-header />
    <v-container>
      <v-row>
        <v-col cols="12" md="12">
          <v-breadcrumbs :items="items">
            <template v-slot:item="{ item }">
              <v-breadcrumbs-item :href="item.href" :disabled="item.disabled">
                <router-link :to="item.href">{{item.text}}</router-link>
              </v-breadcrumbs-item>
            </template>
          </v-breadcrumbs>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" md="10" lg="10" class="text-left">
          <div class="contact-heading py-3">
            <h3>ChinesPod Schoolzone</h3>
            <hr class="seperator" />
          </div>
          <div class="contact-p">
            <p>ChinesePod Schoolzone is an ever-growing library of cloud-based audio and video lessons that your institution or classroom can utilize as an excellent supplementary resource that students can study in their own time.</p>
            <p>With the increasing demand on teachers to prepare lessons, give lectures and grade homework, it is likely that your Institution could benefit from quality supplementary material to extend your core program and reinforce your students’ learning experience.</p>
            <p>We want to extend the use of ChinesePod to every Chinese class, to connect passionate language learners with the best resources and the latest technology to develop a lifetime relationship with the Chinese language and its culture.</p>
          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" md="10">
          <div class="contact-form text-left">
            <div class="contact-heading">
              <h3>If you are interested in using ChinesePod at your institution or classroom.</h3>
              <h4>please leave your details in the form below and we will get back to you shortly :</h4>
            </div>
            <v-form ref="form" v-model="valid">
              <v-row>
                <v-col cols="12" md="6">
                  <v-text-field
                    v-model="organization"
                    prepend-icon="mdi-account-network"
                    :rules="rules"
                    label="Organization"
                    required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" md="6">
                  <v-text-field
                    v-model="name"
                    prepend-icon="mdi-account"
                    :rules="rules"
                    label="Your Name"
                    required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" md="6">
                  <v-text-field
                    v-model="email"
                    prepend-icon="mdi-email-open"
                    :rules="emailRules"
                    label="E-mail"
                    required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" md="6">
                  <v-text-field
                    v-model="job"
                    prepend-icon="mdi-clipboard-account"
                    :rules="rules"
                    label="Job Title"
                    required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" md="6">
                  <v-text-field
                    v-model="phone"
                    prepend-icon="mdi-phone"
                    label="Phone Number (optional)"
                  ></v-text-field>
                </v-col>
              </v-row>
              <div class="mt-5">
                <submit-button text="Submit" btnClass="submit" />
                <v-btn color="default" class="contact-btn" large @click.native="resets()">reset</v-btn>
              </div>
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
      items: [
        {
          text: "SchoolZone",
          disabled: false,
          href: "/"
        },
        {
          text: "Link 1",
          disabled: true,
          href: "/get-access"
        }
      ],
      valid: true,
      organization: "",
      name: "",
      job: "",
      phone: "",
      comments: "",
      email: "",
      rules: [v => !!v || "Field is required"],
      emailRules: [
        v => !!v || "E-mail is required",
        v => /.+@.+\..+/.test(v) || "E-mail must be valid"
      ]
    };
  },
  methods: {
    reset() {
      this.$refs.form.reset();
    },
    submit() {
      if (this.$refs.form.validate()) {
        alert("submitted!");
      }
    }
  }
};
</script>
<style lang="scss" scoped>
#contact {
  padding: 50px 0;
  .seperator {
    width: 50px;
    margin: 10px 0;
    border: 1px solid#cc433b;
  }
  .contact-form {
    margin-top: 20px;
    .contact-heading {
      margin-bottom: 30px;
      h3 {
        font-size: 28px;
        line-height: 40px;
      }
      h4 {
        font-size: 18px;
        font-weight: 400;
      }
    }
    .v-form {
      background: #fbfbfb;
      padding: 40px 30px;
      border-radius: 10px;
      .contact-btn {
        border-radius: 30px;
        padding: 16px 40px;
        margin: 5px;
        font-size: 16px;
        height: unset;
      }
    }
  }
}
</style>