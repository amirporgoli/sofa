<template>
  <v-row>
    <v-col cols="4" v-for="(product,i) in Products" :key="i">
        <v-card max-width="344" class="mx-auto">
            <v-img cover height="200px" :src="product.img"></v-img>
            <v-card-title>{{ product.type }}</v-card-title>
            <v-card-actions>
                <v-btn prepend-icon="mdi mdi-cart">{{ product.money }}</v-btn>
                <v-spacer></v-spacer>
                <v-btn icon="mdi mdi-heart" size="small" variant="text" color="surface-variant"></v-btn>
                <v-btn icon="mdi mdi-share-variant" size="small" variant="text" color="surface-variant"></v-btn>
            </v-card-actions>
        </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
data() {
    return {
        Products: [
        { img: "/src/img/3.jpg", type: "Bedroom", money: "450$" },
        { img: "/src/img/4.jpg", type: "Furniture", money: "600$" },
        { img: "/src/img/5.jpg", type: "Home", money: "430$" },
        { img: "/src/img/6.jpg", type: "Interior", money: "303$" },
        { img: "/src/img/7.jpg", type: "Living Room", money: "700$" },
        { img: "/src/img/8.jpg", type: "Living Room", money: "360$" },
        { img: "/src/img/9.jpg", type: "Living Room", money: "520$" },
        { img: "/src/img/10.jpg", type: "Living Room", money: "360$" },
        { img: "/src/img/2.jpg", type: "Living Room", money: "360$" },
      ],
    }
},
}
</script>

<style>

</style>