<template>
  <v-app dark>
    <Header :color="color" :flat="flat" />
    <v-main>
      <nuxt />
    </v-main>
    <v-btn
      fab
      v-show="fab"
      v-scroll="onScroll"
      dark
      fixed
      bottom
      right
      color="#475C6D"
      @click="toTop"
    >
      <v-icon>mdi-arrow-up</v-icon>
    </v-btn>

    <Footer />
  </v-app>
</template>

<script>
export default {
  head() {
    return {
      title: "Küpçük Hukuk Bürosu | Free UI kit built with Vuetify",
      meta: [
        {
          hid: "description",
          name: "Küpçük Hukuk Bürosu",
          content: "Küpçük Hukuk Bürosu is the best way"
        }
      ]
    };
  },
  data: () => ({
    fab: null,
    color: "",
    flat: null
  }),
  components: {
    Header: () => import("@/layouts/sections/Header"),
    Footer: () => import("@/layouts/sections/Footer")
  },
  created() {
    const top = window.pageYOffset || 0;
    if (top <= 60) {
      this.color = "transparent";
      this.flat = true;
    }
  },
  watch: {
    fab(value) {
      if (value) {
        this.color = "#475C6D";
        this.flat = false;
      } else {
        this.color = "transparent";
        this.flat = true;
      }
    }
  },

  methods: {
    onScroll(e) {
      if (typeof window === "undefined") return;
      const top = window.pageYOffset || e.target.scrollTop || 0;
      this.fab = top > 60;
    },
    toTop() {
      this.$vuetify.goTo(0);
    }
  }
};
</script>

