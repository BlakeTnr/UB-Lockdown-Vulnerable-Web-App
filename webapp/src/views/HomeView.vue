<template>
  <div>
    <v-row justify="center" align="center">
      <v-col>
        <div class="text-h1">Vinnay's Piszaria</div>
      </v-col>
    </v-row>
    <v-carousel cycle>
      <v-carousel-item :src="this.$data.pizza1"> </v-carousel-item>
      <v-carousel-item :src="this.$data.pizza2"> </v-carousel-item>
      <v-carousel-item :src="this.$data.pizza3"> </v-carousel-item>
      <v-carousel-item :src="this.$data.pizza4"> </v-carousel-item>
    </v-carousel>
    <v-spacer></v-spacer>
    <ItemMenu />
  </div>
</template>

<script>
import pizza1 from "../assets/pizza1.jpg";
import pizza2 from "../assets/pizza2.jpg";
import pizza3 from "../assets/pizza3.jpg";
import pizza4 from "../assets/pizza4.png";
import ItemMenu from "../components/ItemMenu.vue";

export default {
  name: "HomeView",
  components: {
    ItemMenu,
  },

  data() {
    return {
      pizza1,
      pizza2,
      pizza3,
      pizza4,
    };
  },
};
</script>
