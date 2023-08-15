<template>
  <v-footer class="footer">
    <v-container>
      <v-row class="py-0 py-md-15">
        <v-col cols="12" sm="12" md="12" lg="3" class="px-xs-0">
          <h4 class="font-weight-regular font-18">Adres</h4>
          <p class="mt-10">
            Çobançeşme Mah. Sanayi Cad. Nish İstanbul Residance C Blok Kat : 6
            Daire : 69 <br />
            Bahçelievler / İstanbul
          </p>
        </v-col>

        <v-col cols="12" sm="12" md="12" lg="3" class="px-xs-0">
          <h4 class="font-weight-regular font-18">Telefon</h4>
          <p class="mt-10 mb-0">Ofis : +000 000 0000</p>
        </v-col>

        <v-col cols="12" sm="12" md="12" lg="3" class="px-xs-0">
          <h4 class="font-weight-regular font-18">Email</h4>
          <p class="mt-10 mb-0">
            Ofis : 
            <a class="dark-link" href="/">...@hotmail.com</a>
          </p>
        </v-col>

        <v-col cols="12" sm="12" md="12" lg="3" class="px-xs-0">
          <h4 class="font-weight-regular font-18">Sosyal Medya</h4>

          <div class="social-icons mt-10">
            <a href="#">
              <i class="mdi mdi-facebook"></i>
            </a>
            <a href="#">
              <i class="mdi mdi-twitter"></i>
            </a>
            <a href="#">
              <i class="mdi mdi-youtube"></i>
            </a>
            <a href="#">
              <i class="mdi mdi-instagram"></i>
            </a>
          </div>
        </v-col>
      </v-row>
      <div class="footer-bottom-bar font-14">
        <div class="d-block d-md-flex align-center">
          <p class="link">
            All Rights Reserved by
            <a href="www.linkedin.com/in/erenbekman" target="_blank">
              Eren Bekman
            </a>
            - {{ new Date().getFullYear() }}
          </p>
          <div class="ml-auto">
            <div class="d-flex align-center">
              <a href="/" class="link px-4">Terms of Use</a>
              <a href="/" class="link px-4">Legal Disclaimer</a>
              <a href="/" class="link px-4">Privacy Policy</a>
            </div>
          </div>
        </div>
      </div>
    </v-container>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      data: []
    };
  },
  components: {}
};
</script>

<style lang="scss">
.link {
  a {
    text-decoration: none;
  }
}
</style>
