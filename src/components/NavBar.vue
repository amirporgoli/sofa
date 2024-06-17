<template>
  <div class="img-1">
    <v-app-bar color="transparent" class="text-white">
    <template v-slot:prepend>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
    </template>
    <v-app-bar-title>Constructor</v-app-bar-title>
    <v-btn append-icon="mdi mdi-chevron-down">Goods</v-btn>
    <v-btn append-icon="mdi mdi-chevron-down">Rooms</v-btn>
    <v-btn append-icon="mdi mdi-chevron-down">Inspiration</v-btn>
    <v-btn append-icon="mdi mdi-chevron-down">News Item</v-btn>
    <v-text-field hide-details flat label="Search Products" density="compact" single-line prepend-inner-icon="mdi mdi-magnify"></v-text-field>
    <v-spacer></v-spacer>
    <v-btn prepend-icon="mdi mdi-account">Account</v-btn>
    <v-btn prepend-icon="mdi mdi-cart">Bag</v-btn>
  </v-app-bar>
    <v-row>
        <v-col cols="4"  class="d-flex justify-center align-center" style="margin-top: 120px;">
            <v-btn color="transparent text-white" prepend-icon="mdi mdi-basket" append-icon="mdi mdi-chevron-down">Living Room</v-btn>
        </v-col>
        <v-col cols="4" class="d-flex justify-center align-center" style="margin-top: 120px;">
            <h1 class="text-white"><strong>Furniture</strong>& furnishings</h1>
        </v-col>
        <v-col cols="4" class="d-flex justify-center align-center" style="margin-top: 120px;">
            <v-btn prepend-icon="mdi mdi-email" color="transparent text-white">Subscribe</v-btn>
        </v-col>
        <v-col cols="12" class="d-flex justify-center align-center" style="margin-top: 90px;">
            <v-btn rounded="xl">Shope now</v-btn>
        </v-col>
    </v-row>
  </div>
</template>

<script>
export default {};
</script>

<style>
.img-1 {
  background: url('/src/img/1.jpg');
  background-size: contain;
  position: absolute;
  height: 300px;
  width: 100%;
  border-radius: 0 0 30% 30%;
}
</style>