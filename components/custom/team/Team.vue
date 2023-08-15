<template>
  <section id="team" class="team-component mini-spacer">
    <v-container>
      <v-row justify="center">
        <v-col cols="12" sm="10" md="9" lg="7">
          <div class="text-center">
            <h2 class="section-title font-weight-medium">
              Deneyimli ve Profesyonel Ekip
            </h2>
            <p>
             Ekip arkadaşlarımızın her biri kendi alanında uzman ve deneyimli kişilerden oluşmaktadır.
            </p>
          </div>
        </v-col>
      </v-row>

      <v-row class="mt-13">
        <v-col cols="12" md="6" lg="3">
          <v-card elevation="0" class="team-card overflow-hidden mb-15">
            <div class="social-overlay">
              <v-img :src="require('@/assets/images/team/t1.jpg')" alt="team" />
              <div class="img-overlay">
                <ul>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-facebook"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-twitter"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-instagram"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-youtube"></i>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
            <div>
              <h5 class="team-title font-weight-medium font-18">
                Michael Doe
              </h5>
              <p class="team-subtitle">Property Specialist</p>
            </div>
            <p>
              You can relay on our amazing features list and also our customer
              services will be great experience.
            </p>
          </v-card>
        </v-col>
        <v-col cols="12" md="6" lg="3">
          <v-card elevation="0" class="team-card overflow-hidden mb-15">
            <div class="social-overlay">
              <v-img :src="require('@/assets/images/team/t2.jpg')" alt="team" />
              <div class="img-overlay">
                <ul>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-facebook"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-twitter"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-instagram"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-youtube"></i>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
            <div>
              <h5 class="team-title font-weight-medium font-18">
                Michael Doe
              </h5>
              <p class="team-subtitle">Property Specialist</p>
            </div>
            <p>
              You can relay on our amazing features list and also our customer
              services will be great experience.
            </p>
          </v-card>
        </v-col>
        <v-col cols="12" md="6" lg="3">
          <v-card elevation="0" class="team-card overflow-hidden mb-15">
            <div class="social-overlay">
              <v-img :src="require('@/assets/images/team/t3.jpg')" alt="team" />
              <div class="img-overlay">
                <ul>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-facebook"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-twitter"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-instagram"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-youtube"></i>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
            <div>
              <h5 class="team-title font-weight-medium font-18">
                Michael Doe
              </h5>
              <p class="team-subtitle">Property Specialist</p>
            </div>
            <p>
              You can relay on our amazing features list and also our customer
              services will be great experience.
            </p>
          </v-card>
        </v-col>
        <v-col cols="12" md="6" lg="3">
          <v-card elevation="0" class="team-card overflow-hidden mb-15">
            <div class="social-overlay">
              <v-img :src="require('@/assets/images/team/t4.jpg')" alt="team" />
              <div class="img-overlay">
                <ul>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-facebook"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-twitter"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-instagram"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="mdi mdi-youtube"></i>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
            <div>
              <h5 class="team-title font-weight-medium font-18">
                Michael Doe
              </h5>
              <p class="team-subtitle">Property Specialist</p>
            </div>
            <p>
              You can relay on our amazing features list and also our customer
              services will be great experience.
            </p>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
import VueScrollReveal from "scrollreveal";
export default {
  name: "Team",
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
