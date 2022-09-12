<template>
  <div class="banner-wrapper">
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="7" lg="6" class="d-flex align-center">
          <div class="text-center text-md-left">
            <h1 class="banner-title font-weight-bold white--text">
              Küpçük Hukuk Bürosu
            </h1>
            <h4 class="banner-subtitle white--text font-weight-regular">
              Kabul görenden değil doğru olandan başla.
              <br />
              - Franz Kafka
            </h4>
            <div class="mt-16 pt-2">
              <v-btn
                class="mr-0 mr-md-8 mb-5 mb-md-0 btn-custom-md btn-banner"
                nuxt
                large
                target="_blank"
                href="https://www.wrappixel.com/templates/nextkit-nuxtjs-free-uikit/"
                elevation="0"
              >
                Keşfet
                <v-icon>mdi-plus</v-icon>
              </v-btn>
            </div>
          </div>
        </v-col>
        <v-col cols="12" md="5" lg="6">
          <v-img
            :src="require('@/assets/images/lawyer/3.png')"
            alt="banner"
            height="500"
            class="banner-logo"
          />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
import VueScrollReveal from "scrollreveal";
export default {
  name: "Banner",
  data() {
    return {};
  },
  mounted() {
    VueScrollReveal().reveal(".banner-title", {
      origin: "left",
      duration: 1000,
      distance: "25rem",
      delay: 300
    });
  }
};
</script>

<style>
@media (max-width: 991px) {
  .banner-logo {
    display: none;
  }
}
</style>
