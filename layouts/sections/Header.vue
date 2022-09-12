<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      app
      dark
      temporary
      src="@/assets/images/logos/bgDrawer.jpeg"
    >
      <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <!-- <img src="@/assets/images/logos/logo.png" alt="Logo" /> -->
            <v-icon>mdi-scale-unbalanced</v-icon>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title class="title">
              Küpçük Hukuk Bürosu</v-list-item-title
            >
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider />

      <v-list dense>
        <v-list-item
          v-for="([icon, text, link], i) in items"
          :key="i"
          link
          @click="$vuetify.goTo(link)"
        >
          <v-list-item-icon class="justify-center">
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="subtitile-1">{{
              text
            }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      :color="color"
      :flat="flat"
      dark
      class="px-15"
      :class="{ expand: flat }"
    >
      <v-toolbar-title>
        <Logo />
      </v-toolbar-title>
      <v-spacer />
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
        class="mr-4"
        v-if="isXs"
      />
      <div v-else>
        <v-btn text @click="$vuetify.goTo('#about')">
          <span class="mr-2">Hakkimizda</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#work')">
          <span class="mr-2">Çalışma Alanları</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#team')">
          <span class="mr-2">Ekibimiz</span>
        </v-btn>
        <v-btn rounded outlined text @click="$vuetify.goTo('#contact')">
          <span class="mr-2">İletişim</span>
        </v-btn>
      </div>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  components: {
    Logo: () => import("@/layouts/sections/Logo")
  },
  data: () => ({
    drawer: null,
    isXs: false,
    items: [
      ["mdi-home-outline", "Hakkımızda", "#about"],
      ["mdi-information-outline", "Ekibimiz", "#team"],
      ["mdi-currency-usd", "Çalışma Alanları", "#work"],
      ["mdi-email-outline", "İletişim", "#contact"]
    ]
  }),
  props: {
    color: String,
    flat: Boolean
  },
  methods: {
    onResize() {
      this.isXs = window.innerWidth < 850;
    }
  },
  watch: {
    isXs(value) {
      if (!value) {
        if (this.drawer) {
          this.drawer = false;
        }
      }
    }
  },
  mounted() {
    this.onResize();
    window.addEventListener("resize", this.onResize, { passive: true });
  }
};
</script>

<style scoped>
.v-toolbar {
  transition: 0.6s !important;
}
.expand {
  height: 80px !important;
  padding-top: 10px;
}
</style>
