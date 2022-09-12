<template>
  <section id="contact" class="mini-spacer">
    <v-container>
      <v-row justify="center">
        <v-col cols="12" sm="10" md="12" lg="8">
          <div>
            <h4 class="font-weight-medium contact-title mt-0">
              Hızlı İletişim
            </h4>
            <form>
              <v-row class="mt-15">
                <v-col cols="12" md="6" class="py-0">
                  <v-text-field
                    label="İsim"
                    outlined
                    v-model="name"
                    placeholder="İsim"
                  ></v-text-field>
                </v-col>
                <v-col cols="12" md="6" class="py-0">
                  <v-text-field
                    label="Email"
                    outlined
                    type="email"
                    v-model="email"
                    placeholder="Email"
                  ></v-text-field>
                </v-col>
                <v-col cols="12" class="py-0">
                  <v-textarea
                    name="message"
                    outlined
                    label="Mesaj"
                    rows="3"
                  ></v-textarea>
                </v-col>
              </v-row>
              <v-btn
                nuxt
                to="/"
                class="btn-custom-md btn-danger-gradient mt-12"
                outlined
                color="white"
                elevation="0"
              >
                Gönder
              </v-btn>
            </form>
          </div>
        </v-col>
        <v-col cols="12" sm="10" md="12" lg="4">
          <div class="primary contact-detail-card">
            <h2 class="detail-title font-weight-medium white--text">
              Küpçük Hukuk Bürosu
            </h2>
            <p class="mt-15 op-8 mb-0 white--text">251 546 9442</p>
            <p class="op-8 mb-8 white--text">info@xx.com</p>
            <p class="mt-15 op-8 mb-0 white--text">
              Çobançeşme Mah. Sanayi Cad. Nish İstanbul Residance C Blok K:6
              D:69
            </p>
            <p class="op-8 mb-0 white--text">Bahçelievler , İstanbul</p>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
export default {
  name: "Contact",
  data() {
    return {
      name: "",
      email: ""
    };
  },
  methods: {}
};
</script>
