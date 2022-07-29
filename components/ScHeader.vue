<template>
  <header class="sc-header z-[3] relative">
    <v-container>
      <sc-navbar />
      <div class="py-16 my-10 d-flex align-center justify-center">
        <div class="text-center">
          <h1 class="font-bold text-6xl white--text leading-[1.3] big-title">
            Self Storage Buisiness <br />
            Buy. Sell. Learn.
          </h1>
          <p class="max-w-[600px] mx-auto text-xl white--text font-medium mt-4">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sit
            sagittis, aliquam non tortor blandit lobortis. blandit
          </p>
          <v-row class="max-w-[680px] mx-auto mt-10">
            <v-col cols="12" md="6">
              <button
                class="primarydark--text secondary sc-btn h-[60px] px-8 d-flex align-center w-full justify-center"
              >
                Sell Your Self Storage
              </button>
            </v-col>
            <v-col cols="12" md="6">
              <button
                class="primarydark--text sc-btn h-[60px] px-8 d-flex align-center white w-full justify-center"
              >
                Active Self Storage Listings
              </button>
            </v-col>
          </v-row>
        </div>
      </div>
    </v-container>
  </header>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped></style>
