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
          class="hidden-sm-and-up p0"
          @click.native="mobMenu = true"
          v-if="!mobMenu"
          style="background:transparent; box-shadow:none;"
        >
          <v-icon color="white">mdi-menu</v-icon>
        </v-btn>
      </template>
      <v-card
        :class="{'open-mob-menu': mobMenu, 'close-mob-menu': !mobMenu}"
        style="background:transparent; box-shadow:none;"
      >
        <v-btn
          v-if="mobMenu"
          icon
          @click.native="mobMenu = false"
          color="white"
          style="margin-right: 10px;"
        >
          <v-icon>mdi-close</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
        <div class="mobNav pt-13">
          <v-expansion-panels multiple focusable>
            <v-expansion-panel style="border-radius: 0">
              <v-expansion-panel-header>
                <div>Lessons</div>
              </v-expansion-panel-header>
              <v-expansion-panel-content>
                <router-link to>Sample Lesssons</router-link>
              </v-expansion-panel-content>
              <v-expansion-panel-content>
                <router-link to>Say it right</router-link>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel style="border-radius: 0" class="mt-0">
              <v-expansion-panel-header>
                <div>Tools</div>
              </v-expansion-panel-header>
              <v-expansion-panel-content>
                <router-link to>Dictionary</router-link>
              </v-expansion-panel-content>
              <v-expansion-panel-content>
                <router-link to>Pronunciation</router-link>
              </v-expansion-panel-content>
              <v-expansion-panel-content>
                <router-link to>Blog</router-link>
              </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel style="border-radius: 0" class="mt-0 text-center">
              <v-expansion-panel-header>
                <div>Schoolzone</div>
              </v-expansion-panel-header>
              <v-expansion-panel-content>
                <router-link to>What is Schoolzone</router-link>
              </v-expansion-panel-content>
              <v-expansion-panel-content>
                <router-link to>How to use Schoolzone</router-link>
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel style="border-radius: 0" class="mt-0 text-center">
              <v-expansion-panel-header>
                <div>Company</div>
              </v-expansion-panel-header>
              <v-expansion-panel-content>
                <router-link to>Why Choose Us</router-link>
              </v-expansion-panel-content>
              <v-expansion-panel-content>
                <router-link to>Contact Us</router-link>
              </v-expansion-panel-content>
              <v-expansion-panel-content>
                <router-link to>Help</router-link>
              </v-expansion-panel-content>
            </v-expansion-panel>
            <v-expansion-panel style="border-radius: 0" class="mt-0 text-center">
              <v-expansion-panel-header>
                <router-link to style="color:#fff;">Login</router-link>
              </v-expansion-panel-header>
            </v-expansion-panel>
          </v-expansion-panels>
          <primary-button class="nav-list" text="Get Access" btnClass="access" />
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
.theme--light {
  &.v-expansion-panels {
    .v-expansion-panel {
      background-color: transparent !important;
      &:before {
        box-shadow: none;
      }
      .v-expansion-panel-header {
        text-align: center;
        color: #fff !important;
        .v-expansion-panel-header__icon {
          display: none;
        }
      }
      .v-expansion-panel-content {
        cursor: pointer;
        background-color: #fff;
        .v-expansion-panel-content__wrap {
          padding: 10px 0 !important;
          a {
            color: #070707;
          }
        }
      }
    }
  }
}
.v-expansion-panel--active > .v-expansion-panel-header {
  min-height: 48px !important;
}
</style>
