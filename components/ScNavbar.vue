<template>
  <div>
    <nav class="d-flex gap-7 white--text align-center py-2 text-xl">
      <sc-logo />
      <v-spacer />
      <div class="d-flex align-center gap-7" v-if="$vuetify.breakpoint.lgAndUp">
        <a class="white--text" v-for="l in links" :key="l.name">{{ l.name }}</a>
        <button class="px-[17px] py-[7px] primarydark--text secondary sc-btn">
          Contact
        </button>
      </div>
      <button
        v-else
        class="secondary rounded-pill h-12 w-12 d-flex align-center justify-center primarydark--text"
        @click="drawer = !drawer"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="icon icon-tabler icon-tabler-menu"
          width="27"
          height="27"
          viewBox="0 0 24 24"
          stroke-width="2"
          stroke="currentColor"
          fill="none"
          stroke-linecap="round"
          stroke-linejoin="round"
        >
          <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
          <line x1="4" y1="8" x2="20" y2="8"></line>
          <line x1="4" y1="16" x2="20" y2="16"></line>
        </svg>
      </button>
    </nav>
    <template v-if="$vuetify.breakpoint.mdAndDown">
      <v-navigation-drawer v-model="drawer" absolute temporary>
        <div class="h-20 my-3 d-flex align-center justify-center">
          <sc-logo />
        </div>
        <v-divider class="mx-4" />
        <v-list dense nav>
          <v-list-item v-for="item in links" :key="item.name">
            <v-list-item-icon>
              <v-icon color="secondary">{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>
                <span class="font-semibold">
                  {{ item.name }}
                </span>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    </template>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      links: [
        {
          name: 'Active Listings',
          icon: 'mdi-package-variant-closed',
        },
        {
          name: 'Sell Your self Storage',
          icon: 'mdi-store',
        },
        {
          name: 'Free Evaluation',
          icon: 'mdi-shield-star',
        },
        {
          name: 'Learn',
          icon: 'mdi-book',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped></style>
