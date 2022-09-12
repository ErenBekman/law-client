<template>
  <section id="banner">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col sm="4" class="hidden-xs-only">
              <v-img
                :src="require('@/assets/images/lawyer/6.svg')"
                class="d-block ml-auto mr-auto"
                max-width="350px"
              />
            </v-col>
            <v-col cols="12" sm="8">
              <h1 class="font-weight-light display-2 mb-2 white--text">
                Hukuk Bürosu
              </h1>
              <h1 class="font-weight-light white--text">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste ex
                animi quod laboriosam vel blanditiis labore alias, aliquid,
                tempora repellendus non.
              </h1>

              <v-btn
                rounded
                outlined
                large
                color="white"
                class="mt-4"
                @click="$vuetify.goTo('#contact')"
              >
                <v-icon class="mr-2">
                  mdi-send
                </v-icon>
                İletişim
              </v-btn>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
#banner {
  background-image: url("~@/assets/images/lawyer/bgDownload.jpeg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 500px;
}
#banner .container,
#banner .row {
  height: 100%;
}
</style>
