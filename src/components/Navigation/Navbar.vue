<template>
  <div id="header">
    <v-toolbar>
      <!-- Website Brand -->
      <v-toolbar-title>
        <v-img src="../../assets/logo.svg" style="width: 160px;" alt />
      </v-toolbar-title>
      <!-- Desktop Navbar -->
      <div class="desktopNav hidden-sm-and-down ml-5 width-100">
        <ul class="nav-list left text-uppercase">
          <li class="nav-item">
            <router-link to>Lessons</router-link>
            <div class="nav-items-dropdown-box lessions">
              <ul
                class="nav-items-dropdown d-flex flex-row justify-center align-center py-5 m-auto"
              >
                <li class="nav-item-dropdown">
                  <router-link to>Sample Lesssons</router-link>
                </li>
                <li class="nav-item-dropdown">
                  <router-link to>Say it right</router-link>
                </li>
              </ul>
            </div>
          </li>
          <li class="nav-item">
            <router-link to>Tools</router-link>
            <div class="nav-items-dropdown-box tools">
              <ul
                class="nav-items-dropdown d-flex flex-row justify-center align-center py-5 m-auto"
              >
                <li class="nav-item-dropdown">
                  <router-link to>Dictionary</router-link>
                </li>
                <li class="nav-item-dropdown">
                  <router-link to>Pronunciation</router-link>
                </li>
                <li class="nav-item-dropdown">
                  <router-link to>Blog</router-link>
                </li>
              </ul>
            </div>
          </li>
          <li class="nav-item">
            <router-link to>Schoolzone</router-link>
            <div class="nav-items-dropdown-box schoolzone">
              <ul
                class="nav-items-dropdown d-flex flex-row justify-center align-center py-5 m-auto"
              >
                <li class="nav-item-dropdown">
                  <router-link to>What is Schoolzone</router-link>
                </li>
                <li class="nav-item-dropdown">
                  <router-link to>How to use Schoolzone</router-link>
                </li>
              </ul>
            </div>
          </li>
        </ul>
        <v-spacer></v-spacer>
        <ul class="nav-list right hidden-sm-and-down">
          <li class="nav-item">
            <router-link to>Company</router-link>
          </li>
          <li class="nav-item">
            <router-link to>Login</router-link>
          </li>
        </ul>
        <primary-button class="nav-list hidden-sm-and-down" text="Get Access" btnClass="access" />
      </div>

      <!-- Mobile Navbar -->
      <template>
        <v-btn
          color="primary"
          tex
          t
          class="hidden-sm-and-up p0"
          @click.native="mobMenu = true"
          v-if="!mobMenu"
        >
          <v-icon>mdi-menu</v-icon>
        </v-btn>
      </template>
      <v-card :class="{'open-mob-menu': mobMenu, 'close-mob-menu': !mobMenu}">
        <v-btn v-if="mobMenu" icon @click.native="mobMenu = false">
          <v-icon>mdi-close</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
        <div class="mobNav pt-13">
          <ul class="nav-list left text-uppercase hidden-sm-and-up">
            <li class="nav-item">
              <router-link to @click.native="dropdown = !dropdown">Lessons</router-link>
              <div
                class="nav-items-dropdown-box lessions"
                :class="{'open-dropdown': dropdown, 'close-dropdown': !dropdown}"
              >
                <ul class="nav-items-dropdown py-5 m-auto">
                  <li class="nav-item-dropdown">
                    <router-link to>Sample Lesssons</router-link>
                  </li>
                  <li class="nav-item-dropdown">
                    <router-link to>Say it right</router-link>
                  </li>
                </ul>
              </div>
            </li>
            <li class="nav-item">
              <router-link to @click.native="dropdown2 = !dropdown2">Tools</router-link>
              <div
                class="nav-items-dropdown-box tools"
                :class="{'open-dropdown': dropdown2, 'close-dropdown': !dropdown2}"
              >
                <ul class="nav-items-dropdown py-5 m-auto">
                  <li class="nav-item-dropdown">
                    <router-link to>Dictionary</router-link>
                  </li>
                  <li class="nav-item-dropdown">
                    <router-link to>Pronunciation</router-link>
                  </li>
                  <li class="nav-item-dropdown">
                    <router-link to>Blog</router-link>
                  </li>
                </ul>
              </div>
            </li>
            <li class="nav-item">
              <router-link to @click.native="dropdown3 = !dropdown3">Schoolzone</router-link>
              <div
                class="nav-items-dropdown-box schoolzone"
                :class="{'open-dropdown': dropdown3, 'close-dropdown': !dropdown3}"
              >
                <ul class="nav-items-dropdown py-5 m-auto">
                  <li class="nav-item-dropdown">
                    <router-link to>What is Schoolzone</router-link>
                  </li>
                  <li class="nav-item-dropdown">
                    <router-link to>How to use Schoolzone</router-link>
                  </li>
                </ul>
              </div>
            </li>
          </ul>
        </div>
      </v-card>
    </v-toolbar>
  </div>
</template>

<script>
import PrimaryButton from "../Buttons/Button";
export default {
  components: {
    PrimaryButton
  },
  data() {
    return {
      navBtn: true,
      mobMenu: false,
      dropdown: false,
      dropdown2: false,
      dropdown3: false
    };
  },
  methods: {
    navIconChange() {
      this.navBtn = !this.navBtn;
    }
  }
};
</script>

<style lang="scss">
@import "../../assets/scss/index.scss";
</style>
