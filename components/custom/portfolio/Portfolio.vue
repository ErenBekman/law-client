<template>
  <section id="work" class="portfolio-component mini-spacer">
    <v-container>
      <v-row justify="center">
        <v-col cols="12" sm="10" md="9" lg="7">
          <div class="text-center">
            <h2 class="section-title font-weight-medium">
              Hizmetlerimiz
            </h2>
            <p>
              Müvekkillerimize, başta Şirketler Hukuku, Vergi Hukuku,
              Uluslararası Ticaret Hukuku, Tahkim, Sözleşmeler Hukuku, İş
              Hukuku, İnşaat Hukuku, Gayrimenkul Hukuku ve İcra İflas Hukuku
              olmak üzere ticari hayatın birçok farklı alanında hizmet
              vermekteyiz.
            </p>
          </div>
        </v-col>
      </v-row>

      <v-row class="mt-13">
        <v-col
          cols="12"
          md="6"
          lg="4"
          v-for="item in portfolios"
          :key="item.id"
        >
          <v-card
            class="portfolio-card overflow-hidden"
            :class="item.id % 2 == 0 ? 'anm-top' : 'anm-bottom'"
          >
            <div class="portfolio-img">
              <img :src="item.img" class="img-fluid img-logo" alt="portfolio" />
            </div>
            <v-card-text>
              <h5 class="font-weight-medium font-18 text--center">
                {{ item.text }}
              </h5>
              <!-- <p class="font-14 mb-0">Book Covers</p> -->
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
import VueScrollReveal from "scrollreveal";
export default {
  name: "Portfolio",
  data() {
    return {
      portfolios: [
        {
          id: 1,
          text: "Ticaret Hukuku",
          img: require("@/assets/images/lawyer/17.png")
        },
        {
          id: 2,
          text: "Ceza Hukuku",
          img: require("@/assets/images/lawyer/15.png")
        },
        {
          id: 3,
          text: "Idare Hukuku",
          img: require("@/assets/images/lawyer/20.svg")
        },
        {
          id: 4,
          text: "Gayrimenkul Hukuku",
          img: require("@/assets/images/lawyer/13.png")
        },
        {
          id: 5,
          text: "Miras Hukuku",
          img: require("@/assets/images/lawyer/23.svg")
        },
        {
          id: 6,
          text: "Aile Hukuku",
          img: require("@/assets/images/lawyer/24.svg")
        }
      ]
    };
  },
  mounted() {
    VueScrollReveal().reveal(".anm-top", {
      origin: "top",
      duration: 1000,
      distance: "25rem",
      delay: 300
    });
    VueScrollReveal().reveal(".anm-bottom", {
      origin: "bottom",
      duration: 1000,
      distance: "25rem",
      delay: 300
    });
  }
};
</script>

<style scoped>
.img-logo {
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  width: 55%;
  height: auto;
  margin-left: 70px;
}
</style>
