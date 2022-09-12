<template>
  <div class="banner1-component">
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="5" lg="5" class="anm-right">
          <v-img :src="require('@/assets/images/lawyer/7.svg')" alt="banner" />
        </v-col>
        <v-col cols="12" md="7" lg="6" class="d-flex align-center anm-left">
          <div class="text-center text-md-left">
            <v-chip small class="bg-dark" text-color="white">
              Creating Brands
            </v-chip>
            <h2
              class="
                  banner1-title
                  font-weight-bold
                  text-uppercase
                "
            >
              Küpçük Hukuk Bürosu
            </h2>
            <p class=" op-8 font-weight-regular">
              Küpçük Hukuk Bürosu olarak, en etkin hukuk çözümlerini pratik bir
              şekilde ve mümkün olan en kısa sürede müvekkillerimize sunmaya,
              müvekkillerimizin yalnızca mevcut hukuki problemlerine yönelik
              değil, gelecekte karşılaşabilecekleri sorunları da önleyecek
              çözümleri üretmeye dikkat ve özen gösteriyor, tüm hizmetlerimizde
              müvekkillerimizin itibar ve gizliliğini en ön plana koyuyoruz.
            </p>
            <div class="mt-16 pt-2">
              <v-btn
                nuxt
                large
                rounded
                to="/"
                class="btn-custom-md btn-color-white"
                depressed
                elevation="0"
              >
                Hemen İletişime Geç
              </v-btn>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
import VueScrollReveal from "scrollreveal";
export default {
  name: "Banner1",
  data() {
    return {};
  },
  mounted() {
    VueScrollReveal().reveal(".anm-left", {
      origin: "left",
      duration: 1000,
      distance: "25rem",
      delay: 300
    });
    VueScrollReveal().reveal(".anm-right", {
      origin: "right",
      duration: 1000,
      distance: "25rem",
      delay: 300
    });
  }
};
</script>
