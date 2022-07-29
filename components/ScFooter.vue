<template>
  <footer class="pt-[5rem] pb-7">
    <v-container>
      <v-row>
        <v-col cols="12" lg="3">
          <h2 class="font-semibold text-[22px] d-flex align-center gap-2">
            <svg
              width="30"
              height="28"
              viewBox="0 0 30 28"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M0 1.71875C0 0.769511 0.769511 0 1.71875 0H28.2812C29.2305 0 30 0.769511 30 1.71875C30 2.66799 29.2305 3.4375 28.2812 3.4375H1.71875C0.769511 3.4375 0 2.66799 0 1.71875ZM5.04545 4.8125C3.3886 4.8125 2.04545 6.15565 2.04545 7.8125V24.5C2.04545 26.1569 3.3886 27.5 5.04545 27.5H24.9545C26.6114 27.5 27.9545 26.1569 27.9545 24.5V7.8125C27.9545 6.15565 26.6114 4.8125 24.9545 4.8125H5.04545ZM19.7727 9.96875C19.7727 10.5383 19.311 11 18.7415 11H10.5767C10.0072 11 9.54545 10.5383 9.54545 9.96875C9.54545 9.39921 10.0072 8.9375 10.5767 8.9375H18.7415C19.311 8.9375 19.7727 9.39921 19.7727 9.96875Z"
                fill="#1849C6"
              />
            </svg>

            StorageConnect
          </h2>
          <p class="mt-5">
            Nam posuere accumsan porta. Integer id orci sed ante tincidunt
            tincidunt sit amet sed libero.
          </p>
          <p class="mt-8">© StorageConnect 2022, All Rights Reserved</p>
        </v-col>
        <v-col cols="12" lg="3">
          <h3 class="text-uppercase text-lg font-bold mb-[24px]">
            Quick Links
          </h3>
          <a class="black--text d-block mb-5"> Active Listings </a>
          <a class="black--text d-block mb-5"> Self your Self Storage </a>
          <a class="black--text d-block mb-5"> Free Evaluation </a>
          <a class="black--text d-block mb-5"> Learn </a>
        </v-col>
        <v-col cols="12" lg="3">
          <h3 class="text-uppercase text-lg font-bold mb-[24px]">Newsleter</h3>
          <p class="mt-5">Get latest updates right in your inbox</p>
          <div class="sc-input mb-5">
            <input type="text" placeholder="Enter your email" class="ps-3" />
          </div>
          <button
            class="white--text primary sc-btn h-[60px] d-flex align-center px-8 justify-center gap-3"
          >
            Subscribe Now
          </button>
        </v-col>
        <v-col cols="12" lg="3">
          <h3 class="text-uppercase text-lg font-bold mb-[24px]">
            Let's get social
          </h3>
          <div class="d-flex gap-4 mb-7">
            <div
              class="h-9 w-9 primary rounded-circle d-flex align-center justify-center"
            >
              <v-icon color="white">{{ mdiFacebook }}</v-icon>
            </div>
            <div
              class="h-9 w-9 primary rounded-circle d-flex align-center justify-center"
            >
              <v-icon color="white">{{ mdiLinkedin }}</v-icon>
            </div>
            <div
              class="h-9 w-9 primary rounded-circle d-flex align-center justify-center"
            >
              <v-icon color="white">{{ mdiTwitter }}</v-icon>
            </div>
            <div
              class="h-9 w-9 primary rounded-circle d-flex align-center justify-center"
            >
              <v-icon color="white">{{ mdiInstagram }}</v-icon>
            </div>
          </div>
          <v-select
            :append-icon="mdiChevronDown"
            :prepend-inner-icon="mdiEarth"
            dense
            :items="items"
            v-model="lang"
            style="max-width: 200px"
            outlined
          />
        </v-col>
      </v-row>
    </v-container>
  </footer>
</template>

<script>
import {
  mdiFacebook,
  mdiLinkedin,
  mdiTwitter,
  mdiInstagram,
  mdiChevronDown,
  mdiEarth,
} from '@mdi/js'
export default {
  data() {
    return {
      lang: 'English - En',
      items: ['English - En', 'francais - Fr', 'espanol - Es'],
      mdiFacebook,
      mdiLinkedin,
      mdiTwitter,
      mdiInstagram,
      mdiChevronDown,
      mdiEarth,
    }
  },
}
</script>

<style lang="scss" scoped></style>
