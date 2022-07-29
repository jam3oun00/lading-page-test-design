<template>
  <div>
    <sc-header />
    <section class="my-16 pt-md-16 text-center relative">
      <svg
        class="absolute top-[-220px] left-0"
        width="206"
        height="342"
        viewBox="0 0 206 342"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <circle
          opacity="0.4"
          cx="35"
          cy="171"
          r="141"
          stroke="#E8EFFF"
          stroke-width="60"
        />
      </svg>

      <v-container>
        <h1 class="font-semibold text-4xl mb-4 primarydark--text leading-[1.3]">
          Featured Self Storages
        </h1>
        <p class="text-lg max-w-[760px] mx-auto mb-4">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc tortor
          sapien sagittis maecenas tincidunt. Quis pretium ornare
        </p>
        <swiper
          ref="featuredSelfStoragesSwiper"
          class="mt-4"
          :options="swiperOptions"
          navigation
        >
          <swiper-slide v-for="(item, i) in featuredSelfStorages" :key="i">
            <div class="bg-[#F6F8FD] rounded-[10px] pa-4">
              <img
                :src="item.image"
                class="h-[266px] rounded-[10px] w-full d-block ma-0 object-cover"
              />
              <div class="mt-4 d-flex flex-column gap-2">
                <div class="d-flex gap-2 align-center">
                  <img src="@/assets/icons/map.svg" />
                  <span class="font-semibold text-2xl">
                    {{ item.name }}
                  </span>
                </div>

                <div class="d-flex gap-2 align-center">
                  <img src="@/assets/icons/units.svg" />
                  <span class="text-lg">
                    Total Units: {{ item.total_units }}
                  </span>
                </div>

                <div class="d-flex gap-2 align-center">
                  <img src="@/assets/icons/occupancy.svg" />
                  <span class="text-lg">
                    Occupancy: {{ item.occupancy }}%
                  </span>
                </div>

                <div class="d-flex gap-2 align-center">
                  <img src="@/assets/icons/squire.svg" />
                  <span class="text-lg"> Size: {{ item.Size }} </span>
                </div>
                <div class="my-4 d-flex">
                  <button
                    class="white--text primary sc-btn h-[60px] mx-8 d-flex align-center w-full justify-center"
                  >
                    View More Detail
                  </button>
                </div>
              </div>
            </div>
          </swiper-slide>
          <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
      </v-container>
    </section>
    <secion>
      <v-container>
        <div class="text-center mb-16">
          <h1 class="font-bold text-4xl mb-4 leading-[1.3]">
            Active Listing Self Storages
          </h1>
          <p class="text-lg max-w-[760px] mx-auto">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc tortor
            sapien sagittis maecenas tincidunt. Quis pretium ornare
          </p>
        </div>
        <v-row class="details-box pa-9 mb-14 mx-0">
          <v-col cols="12" md="12" lg="5">
            <div class="sc-input">
              <img src="@/assets/icons/map.svg" />
              <input type="text" placeholder="Search location" />
            </div>
          </v-col>
          <v-col cols="12" md="9" lg="5">
            <v-row>
              <v-col cols="12" md="6">
                <div class="sc-input">
                  <img src="@/assets/icons/units.svg" />
                  <input type="text" placeholder="Unit Count" />
                </div>
              </v-col>
              <v-col cols="12" md="6">
                <div class="sc-input">
                  <img src="@/assets/icons/occupancy.svg" />
                  <input type="text" placeholder="Occupancy" />
                  <span> % </span>
                </div>
              </v-col>
            </v-row>
          </v-col>
          <v-col cols="12" md="3" lg="2">
            <button
              class="primarydark--text secondary h-[60px] rounded-[10px] px-3 d-flex align-center w-full justify-center gap-3 text-xl"
            >
              <svg
                width="20"
                height="20"
                viewBox="0 0 20 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M19 19L14.7501 14.7425M17.1053 9.05263C17.1053 11.1883 16.2569 13.2365 14.7467 14.7467C13.2365 16.2569 11.1883 17.1053 9.05263 17.1053C6.91694 17.1053 4.86872 16.2569 3.35856 14.7467C1.8484 13.2365 1 11.1883 1 9.05263C1 6.91694 1.8484 4.86872 3.35856 3.35856C4.86872 1.8484 6.91694 1 9.05263 1C11.1883 1 13.2365 1.8484 14.7467 3.35856C16.2569 4.86872 17.1053 6.91694 17.1053 9.05263V9.05263Z"
                  stroke="#000103"
                  stroke-opacity="0.7"
                  stroke-width="2"
                  stroke-linecap="round"
                />
              </svg>

              Search
            </button>
          </v-col>
        </v-row>
      </v-container>
    </secion>
    <section>
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="4"
            v-for="(item, i) in featuredSelfStorages"
            :key="i"
          >
            <div class="bg-[#F6F8FD] rounded-[10px] pa-4 self-storages-box">
              <img
                :src="item.image"
                class="h-[266px] rounded-[10px] w-full d-block ma-0 object-cover"
              />
              <div class="mt-4 d-flex flex-column gap-2">
                <div class="d-flex gap-2 align-center">
                  <img src="@/assets/icons/map.svg" />
                  <span class="font-semibold text-2xl">
                    {{ item.name }}
                  </span>
                </div>

                <div class="d-flex gap-2 align-center">
                  <img src="@/assets/icons/units.svg" />
                  <span class="text-lg">
                    Total Units: {{ item.total_units }}
                  </span>
                </div>

                <div class="d-flex gap-2 align-center">
                  <img src="@/assets/icons/occupancy.svg" />
                  <span class="text-lg">
                    Occupancy: {{ item.occupancy }}%
                  </span>
                </div>

                <div class="d-flex gap-2 align-center">
                  <img src="@/assets/icons/squire.svg" />
                  <span class="text-lg"> Size: {{ item.Size }} </span>
                </div>
                <div class="my-4 d-flex">
                  <button
                    class="white--text primary sc-btn h-[60px] mx-8 d-flex align-center w-full justify-center"
                  >
                    View More Detail
                  </button>
                </div>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="self-storage-for-sale overflow-hidden relative mt-14">
      <svg
        class="absolute bottom-0 left-0 z-[2]"
        width="135"
        height="183"
        viewBox="0 0 135 183"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <circle
          opacity="0.1"
          cx="-15"
          cy="150"
          r="120"
          stroke="#1849C6"
          stroke-width="60"
        />
      </svg>

      <v-container class="relative pt-12 overflow-hidden">
        <div class="pb-[200px]">
          <button
            class="primarydark--text secondary sc-btn h-[80px] px-16 d-flex align-center justify-center mx-auto"
          >
            View More Listings
          </button>
        </div>
        <v-row align="center">
          <v-col cols="12" md="6">
            <div class="mb-16">
              <h1 class="text-4xl primarydark--text font-bold leading-[1.3]">
                Do you have a Self Storage for Sale?
              </h1>
              <p class="text-lg max-w-[760px] mt-4 mb-8">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc
                tortor sapien sagittis maecenas tincidunt. Quis pretium ornare
                id diam amet proin scelerisque nunc.
              </p>
              <button
                class="white--text primary sc-btn h-[60px] d-flex align-center px-8 justify-center"
              >
                Sell Your Self Storage
              </button>
            </div>
          </v-col>
          <v-col cols="12" md="6" class="py-0">
            <img src="@/assets/images/frame1.png" />
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="buy-a-self-storage pt-[340px] mt-[-220px] relative z-[3]">
      <v-container>
        <v-row align="center" class="flex-column-reverse flex-md-row">
          <v-col cols="12" md="6" class="py-0">
            <img src="@/assets/images/buy-storage-image.png" />
          </v-col>
          <v-col cols="12" md="6">
            <div class="md:mb-[120px]">
              <h1 class="text-4xl primarydark--text font-bold leading-[1.3]">
                Do you want to buy a Self Storage?
              </h1>
              <p class="text-lg max-w-[760px] mt-4 mb-8">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc
                tortor sapien sagittis maecenas tincidunt. Quis pretium ornare
                id diam amet proin scelerisque nunc.
              </p>
              <button
                class="white--text primary sc-btn h-[60px] d-flex align-center px-8 justify-center"
              >
                Buy a Self Storage
              </button>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section
      class="learn pt-[100px] mt-[-140px] md:mt-[-150px] relative z-[3] overflow-hidden"
    >
      <svg
        class="absolute z-[-1] top-[10%] right-0"
        width="76"
        height="172"
        viewBox="0 0 76 172"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <circle
          opacity="0.2"
          cx="86"
          cy="86"
          r="66"
          stroke="white"
          stroke-width="40"
        />
      </svg>
      <svg
        class="absolute z-[-1] bottom-[10%] left-0"
        width="83"
        height="294"
        viewBox="0 0 83 294"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <circle
          opacity="0.2"
          cx="-64"
          cy="147"
          r="117"
          stroke="white"
          stroke-width="60"
        />
      </svg>

      <div class="overlay pt-[100px] overflow-hidden">
        <v-container>
          <div class="text-center mb-16 white--text">
            <h1
              class="font-bold text-4xl mb-5 leading-[1.3] max-w-[800px] mx-auto"
            >
              Learn Everything About Buying, Selling, and Operating a Self
              Storage
            </h1>
            <p class="text-lg max-w-[500px] mx-auto">
              Learn about literally anything to know about Selling or Buying a
              Self Storage
            </p>
          </div>
          <v-row>
            <v-col cols="12" md="6" lg="3" v-for="n in 4" :key="n">
              <div class="bg-[#F6F8FD] rounded-[10px] pa-1">
                <img
                  src="https://media.istockphoto.com/photos/taking-better-control-with-technology-picture-id1304746031?b=1&k=20&m=1304746031&s=170667a&w=0&h=ZVlV_dzpKCd5OcH0sH0XaOB0sTELLN8mU6_2Lv7vhoc="
                  class="h-[266px] squeezed-img overflow-hidden w-full d-block ma-0 object-cover"
                />
                <div class="mt-4 d-flex flex-column gap-2 px-2">
                  <h3 class="d-flex gap-2 align-center font-semibold text-xl">
                    Everything you need to know about how to buy a Self Storage
                  </h3>
                  <div class="d-flex justify-space-between">
                    <div class="d-flex gap-2 align-center">
                      <svg
                        width="18"
                        height="18"
                        viewBox="0 0 18 18"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M8.991 0C4.023 0 0 4.032 0 9C0 13.968 4.023 18 8.991 18C13.968 18 18 13.973 18 9C18 4.02695 13.968 0 8.991 0ZM9 16.2C5.022 16.2 1.8 12.978 1.8 9C1.8 5.022 5.022 1.8 9 1.8C12.978 1.8 16.2 5.022 16.2 9C16.2 12.978 12.978 16.2 9 16.2ZM9.45 4.5H8.1V9.9L12.825 12.735L13.5 11.628L9.45 9.225V4.5Z"
                          fill="#000103"
                          fill-opacity="0.7"
                        />
                      </svg>
                      5hrs ago
                    </div>
                    <div class="d-flex gap-2 align-center">
                      <svg
                        width="18"
                        height="18"
                        viewBox="0 0 18 18"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M9.12843 17.9989C9.61117 17.9983 10.0744 17.808 10.418 17.469L16.8261 11.0509C16.9906 10.8874 17.0931 10.6719 17.1161 10.4411L17.9958 1.09388C18.0093 0.947454 17.9903 0.799861 17.9402 0.661621C17.89 0.523381 17.8101 0.397898 17.7059 0.294116C17.6021 0.189949 17.4766 0.109958 17.3384 0.0598464C17.2001 0.0097344 17.0525 -0.00926534 16.9061 0.00420171L7.55889 0.883941C7.32815 0.906929 7.11257 1.00942 6.94907 1.17385L0.530979 7.58195C0.190945 7.92301 0 8.38497 0 8.86657C0 9.34818 0.190945 9.81013 0.530979 10.1512L7.84881 17.469C8.18882 17.8074 8.64872 17.9978 9.12843 17.9989ZM15.1266 9.89127L9.12843 15.8895L2.08052 8.84158L8.07874 2.84336L15.8864 2.11358L15.1266 9.89127Z"
                          fill="#000103"
                          fill-opacity="0.7"
                        />
                        <path
                          d="M11.4973 8.00293C10.6689 8.00293 9.99728 7.33136 9.99728 6.50293C9.99728 5.6745 10.6689 5.00293 11.4973 5.00293C12.3257 5.00293 12.9973 5.6745 12.9973 6.50293C12.9973 7.33136 12.3257 8.00293 11.4973 8.00293Z"
                          fill="#000103"
                          fill-opacity="0.7"
                        />
                      </svg>
                      Buy
                    </div>
                    <div class="d-flex gap-2 align-center">
                      <img
                        class="rounded-circle border-2 h-5 w-5 overflow-hidden"
                        src="https://i.pinimg.com/280x280_RS/11/ef/1a/11ef1abcec1ba1df7bb6e536ce58792d.jpg"
                      />
                      Raza
                    </div>
                  </div>
                  <div class="my-4 d-flex">
                    <button
                      class="white--text primary sc-btn h-[46px] mx-2 d-flex align-center w-full justify-center"
                    >
                      <span class="font-semibold"> Read More</span>
                    </button>
                  </div>
                </div>
              </div>
            </v-col>
          </v-row>
          <button
            class="primarydark--text secondary sc-btn h-[80px] px-10 my-[100px] d-flex align-center justify-center mx-auto"
          >
            Explore the Learning Section
          </button>
        </v-container>
      </div>
    </section>
    <section class="buy-a-self-storage py-[250px] accent">
      <v-container>
        <div class="write-to-us-box d-flex align-center relative">
          <svg
            width="105"
            height="105"
            viewBox="0 0 105 105"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            class="absolute bottom-[-45px] left-[-45px] z-[1]"
          >
            <circle
              opacity="0.7"
              cx="52.5"
              cy="52.5"
              r="42.5"
              stroke="#FFCE31"
              stroke-width="20"
            />
          </svg>
          <svg
            class="absolute top-[-55px] right-[4rem] z-[1]"
            width="112"
            height="96"
            viewBox="0 0 112 96"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              opacity="0.43"
              d="M99.8873 17.85L32.0608 0.542299C28.206 -0.441337 24.1184 0.146599 20.6972 2.17677C17.276 4.20693 14.8013 7.51303 13.8177 11.3678L1.45501 59.8153C0.471374 63.67 1.05931 67.7576 3.08948 71.1789C5.11964 74.6001 8.42574 77.0747 12.2805 78.0584L80.107 95.3661C83.9618 96.3497 88.0493 95.7618 91.4706 93.7316C94.8918 91.7015 97.3665 88.3954 98.3501 84.5407L110.713 36.0931C111.696 32.2384 111.108 28.1508 109.078 24.7296C107.048 21.3083 103.742 18.8337 99.8873 17.85V17.85ZM97.4148 27.5396L60.3978 41.1599C59.5528 41.3971 58.6602 41.4078 57.8097 41.1908C56.9593 40.9738 56.181 40.5368 55.553 39.9236L29.5882 10.2318L97.4148 27.5396Z"
              fill="white"
            />
          </svg>

          <div
            class="d-flex align-center justify-space-around gap-3 relative z-[2]"
          >
            <div>
              <h1 class="text-4xl primarydark--text font-bold leading-[1.3]">
                Any Queries? Reach Out to Us
              </h1>
              <p class="text-lg max-w-[760px] mt-3 mb-8">
                Feel free to write to us, we are happy to help you
              </p>
            </div>
            <button
              class="white--text primary sc-btn h-[60px] d-flex align-center px-8 justify-center gap-3"
            >
              Write to Us
              <svg
                width="16"
                height="20"
                viewBox="0 0 16 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M0 19.3102L16 10.0001L0 0.689941V7.93114L11.4615 10.0001L0 12.069V19.3102Z"
                  fill="white"
                />
              </svg>
            </button>
          </div>
        </div>
      </v-container>
    </section>
    <sc-footer />
  </div>
</template>

<script>

import placeholderCarouselImage from '@/assets/images/unsplash_OpV94f2edwE.jpg'
export default {
  data() {
    return {
      
      featuredSelfStorages: [
        {
          image: placeholderCarouselImage,
          name: 'Jersy City, NJ',
          total_units: 89,
          occupancy: 50,
          Size: '40,233 Sq Ft',
        },
        {
          image: placeholderCarouselImage,
          name: 'Jersy City, NJ',
          total_units: 89,
          occupancy: 50,
          Size: '40,233 Sq Ft',
        },
        {
          image: placeholderCarouselImage,
          name: 'Jersy City, NJ',
          total_units: 89,
          occupancy: 50,
          Size: '40,233 Sq Ft',
        },
        {
          image: placeholderCarouselImage,
          name: 'Jersy City, NJ',
          total_units: 89,
          occupancy: 50,
          Size: '40,233 Sq Ft',
        },
        {
          image: placeholderCarouselImage,
          name: 'Jersy City, NJ',
          total_units: 89,
          occupancy: 50,
          Size: '40,233 Sq Ft',
        },
        {
          image: placeholderCarouselImage,
          name: 'Jersy City, NJ',
          total_units: 89,
          occupancy: 50,
          Size: '40,233 Sq Ft',
        },
      ],
      swiperOptions: {
        slidesPerView: 1,
        breakpoints: {
          320: {
            slidesPerView: 1,
            spaceBetween: 20,
          },
          768: {
            slidesPerView: 2,
            spaceBetween: 20,
          },
          1024: {
            slidesPerView: 3,
            spaceBetween: 20,
          },
        },
        // loop: true,
        pagination: {
          el: '.swiper-pagination',
          type: 'bullets',
          clickable: true,
        },
      },
    }
  },
}
</script>

<style lang="scss"></style>
