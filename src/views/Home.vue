<template>
  <v-app>
    <NavBar />
    <v-main>
      <v-container>
        <v-card flat style="margin-top: 250px">
          <v-tabs
            color="deep-purple-accent-4"
            align-tabs="center"
            v-model="tab"
          >
            <v-tab :value="1">Newest</v-tab>
            <v-tab :value="2">Highest Rated</v-tab>
            <v-tab :value="3">Low price to Hight</v-tab>
            <v-tab :value="4">Low price to Low</v-tab>
            <v-tab :value="5">Delivery and Returns Products</v-tab>
          </v-tabs>
          <v-window v-model="tab">
            <v-window-item v-for="n in 5" :key="n" :value="n">
              <v-container>
                <v-row>
                  <v-col cols="12" sm="9">
                    <products />
                  </v-col>
                  <v-col cols="12" sm="3">
                    <v-toolbar color="transparent">
                      categories
                      <v-spacer></v-spacer>
                      <v-btn icon="mdi mdi-chevron-down"></v-btn>
                    </v-toolbar>
                    <v-row>
                      <v-col cols="6">
                        <v-checkbox
                          v-model="ex4"
                          label="Sofa"
                          color="info"
                          value="success"
                          hide-details
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="6">
                        <v-checkbox
                          v-model="ex4"
                          label="Sofa"
                          color="info"
                          value="success"
                          hide-details
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="6">
                        <v-checkbox
                          v-model="ex4"
                          label="Bathrooms"
                          color="info"
                          value="success"
                          hide-details
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="6">
                        <v-checkbox
                          v-model="ex4"
                          label="Bathrooms"
                          color="info"
                          value="success"
                          hide-details
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="6">
                        <v-checkbox
                          v-model="ex4"
                          label="Beds"
                          color="info"
                          value="success"
                          hide-details
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="6">
                        <v-checkbox
                          v-model="ex4"
                          label="Beds"
                          color="info"
                          value="success"
                          hide-details
                        ></v-checkbox>
                      </v-col>
                    </v-row>
                    <v-toolbar color="transparent">
                      colors
                      <v-spacer></v-spacer>
                      <v-btn icon="mdi mdi-chevron-down"></v-btn>
                    </v-toolbar>
                    <v-avatar color="#808080" class="ml-1"></v-avatar>
                    <v-avatar color="#DBEBCE" class="ml-1"></v-avatar>
                    <v-avatar color="#EBDFD1" class="ml-1"></v-avatar>
                    <v-avatar color="#E6C5B8" class="ml-1"></v-avatar>
                    <v-avatar color="#D5CAB4" class="ml-1"></v-avatar>
                    <v-avatar color="#E6C5B8" class="ml-1 mt-3"></v-avatar>
                    <v-avatar color="#E0E1E0" class="ml-1 mt-3"></v-avatar>
                    <v-avatar color="#E2BAB6" class="ml-1 mt-3"></v-avatar>
                    <v-avatar color="#CCD0E0" class="ml-1 mt-3"></v-avatar>
                    <v-avatar color="#8B9DC2" class="ml-1 mt-3"></v-avatar>
                    <v-avatar color="#959DB6" class="ml-1 mt-3"></v-avatar>
                    <v-avatar color="#CFE7EB" class="ml-1 mt-3"></v-avatar>
                    <v-toolbar color="transparent">
                      Materials
                      <v-spacer></v-spacer>
                      <v-btn icon="mdi mdi-chevron-down"></v-btn>
                    </v-toolbar>
                    <v-row>
                      <v-col cols="6" sm="6" md="6">
                        <v-checkbox
                          hide-details
                          v-model="ex4"
                          label="Wood"
                          value="success"
                          color="success"
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="6" sm="6" md="6">
                        <v-checkbox
                          hide-details
                          v-model="ex4"
                          label="Metal"
                          value="info"
                          color="success"
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="6" sm="6" md="6">
                        <v-checkbox
                          hide-details
                          v-model="ex4"
                          label="Leathers"
                          value="red"
                          color="success"
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="6" sm="6" md="6">
                        <v-checkbox
                          hide-details
                          v-model="ex5"
                          label="Fabrics"
                          value="success"
                          color="success"
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="6" sm="6" md="6">
                        <v-checkbox
                          hide-details
                          v-model="ex5"
                          label="Bathrooms"
                          value="info"
                          color="success"
                        ></v-checkbox>
                      </v-col>
                      <v-col cols="6" sm="6" md="6">
                        <v-checkbox
                          hide-details
                          v-model="ex5"
                          label="Metal"
                          value="info"
                          color="success"
                        ></v-checkbox>
                      </v-col>
                    </v-row>
                    <v-toolbar color="transparent">
                      Store Raitings
                      <v-spacer></v-spacer>
                      <v-btn icon="mdi mdi-chevron-down"></v-btn>
                    </v-toolbar>
                    <v-rating v-model="r1" color="yellow-darken-3"></v-rating>
                    <v-rating v-model="r2" color="yellow-darken-3"></v-rating>
                    <v-rating v-model="r3" color="yellow-darken-3"></v-rating>
                    <v-toolbar color="transparent">
                      price
                      <v-spacer></v-spacer>
                      <v-btn icon="mdi mdi-chevron-down"></v-btn>
                    </v-toolbar>
                    <v-slider thumb-label="always" color="pink" v-model="slider2"></v-slider>
                  </v-col>
                </v-row>
              </v-container>
            </v-window-item>
          </v-window>
        </v-card>
      </v-container>
    </v-main>
    <Footer />
  </v-app>
</template>

<script setup>
import NavBar from "@/components/NavBar.vue";
import Products from "@/components/Products.vue";
import Footer from "@/components/Footer.vue";
</script>
<script>
export default {
  components: { Products },
  data() {
    return {
      tab: null,
      r1: 4,
      r2: 3,
      r3: 2,
      slider2: 60,
      ex4: [
        "red",
        "indigo",
        "orange",
        "primary",
        "secondary",
        "success",
        "info",
        "warning",
        "error",
        "red darken-3",
        "indigo darken-3",
        "orange darken-3",
      ],
      ex5: [
        "red",
        "indigo",
        "orange",
        "primary",
        "secondary",
        "success",
        "info",
        "warning",
        "error",
        "red darken-3",
        "indigo darken-3",
        "orange darken-3",
      ],
    };
  },
};
</script>