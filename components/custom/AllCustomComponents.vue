<template>
  <div>
    <v-main class="pt-0">
      <HeaderText />
      <Banner1 />
      <Banner2 />
      <Portfolio />
      <Banner3 />
      <Team />
      <Testimonial />
      <Contact />
      <Map />
      <v-divider></v-divider>
    </v-main>
  </div>
</template>

<script>
export default {
  name: "AllCustomComponents",

  data() {
    return {};
  },
  components: {
    HeaderText: () => import("@/components/custom/header/HeaderText"),
    Banner1: () => import("@/components/custom/banner/Banner1"),
    Banner2: () => import("@/components/custom/banner/Banner2"),
    Banner3: () => import("@/components/custom/banner/Banner3"),
    Portfolio: () => import("@/components/custom/portfolio/Portfolio"),
    Map: () => import("@/components/custom/maps/map"),
    Team: () => import("@/components/custom/team/Team"),
    Testimonial: () => import("@/components/custom/testimonial/Testimonial"),
    Contact: () => import("@/components/custom/contact/Contact")
  }
};
</script>

<style scoped>
.v-main {
  /* background-image: url("~@/assets/images/lawyer/bgMain.png"); */
  background-attachment: fixed;
  background-position: center;
  background-size: cover;
}
</style>
