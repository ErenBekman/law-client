<template>
  <div>
    <div class="map">
      <v-container>
        <v-row justify="center">
          <v-col cols="12" sm="10" md="9" lg="7">
            <div class="text-center">
              <h2 class="map-title font-weight-medium">
                Adresimize Ulaşmak İçin Haritayı Kullanabilirsiniz
              </h2>
              <p>
                Çobançeşme Mah. Sanayi Cad. Nish İstanbul Residance C Blok Kat : 6 Daire : 69 Bahçelievler / İstanbul
              </p>
            </div>
          </v-col>
        </v-row>
        <v-row justify="center">
          <v-col cols="12" sm="10" md="9" lg="9">
            <GmapMap
              :center="center"
              :zoom="17"
              map-type-id="terrain"
              style="width: 900px; height: 450px"
            >
              <GmapMarker
                :key="index"
                v-for="(m, index) in markers"
                :position="m.position"
                :clickable="true"
                :draggable="true"
                @click="center = m.position"
              />
            </GmapMap>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  name: "map",
  data() {
    return {
      center: { lat: 41.0573559, lng: 28.8338317 },
      markers: [{ position: { lat: 41.0573559, lng: 28.8338317 } }]
    };
  },
  methods: {}
};
</script>
