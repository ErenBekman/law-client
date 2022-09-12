<template>
  <div class="logo">
    <nuxt-link to="/" tag="p" class="d-flex">
      <v-icon x-large>mdi-scale-unbalanced</v-icon>
      <p class="font-weight-thin logo-text">
        Küpçük Hukuk <br />
        Bürosu
      </p>
      <!-- <v-img
        :src="require('@/assets/images/logos/logo2.png')"
        alt="logo"
        class="logo"
      /> -->
    </nuxt-link>
  </div>
</template>

<script>
export default {
  name: "Logo",

  data() {
    return {};
  }
};
</script>

<style lang="scss">
.logo a {
  display: flex;
}

.logo {
  width: 150px;
  height: 50px;
}
.logo-text {
  font-size: 15px;
}
</style>
