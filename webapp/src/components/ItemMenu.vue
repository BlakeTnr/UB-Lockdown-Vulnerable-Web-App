<template lang="">
  <div>
    <p class="text-h2">Menu</p>
    <v-row>
      <v-col md="6">
        <v-card>
          <v-card-title>Pizza</v-card-title>
          <v-card-subtitle>$15</v-card-subtitle>
          <v-img max-height="200px" :src="Pizza"></v-img>
          <v-card-text
            >Get a full pie for just $15! Our oven fresh pizza is sure to make
            your mouth water for more.</v-card-text
          >
        </v-card>
        <v-card>
          <v-card-title>Salad</v-card-title>
          <v-card-subtitle>$5</v-card-subtitle>
          <v-img max-height="200px" :src="Salad"></v-img>
          <v-card-text
            >Want to stick to the healthy side? We got you covered too with a
            healthy salad.</v-card-text
          >
        </v-card>
        <v-card>
          <v-card-title>Subs & Sandwiches</v-card-title>
          <v-card-subtitle>$7</v-card-subtitle>
          <v-img max-height="200px" :src="Sub"></v-img>
          <v-card-text
            >Want a taste of everything? Enjoy our homemade specialty sub sauce
            as well.</v-card-text
          >
        </v-card>
      </v-col>
      <v-col md="6">
        <v-card>
          <v-card-title>Wings</v-card-title>
          <v-card-subtitle>$12</v-card-subtitle>
          <v-img max-height="200px" :src="Wings"></v-img>
          <v-card-text
            >Want a few crispy wings? Get a pack of 12 for just
            $12!</v-card-text
          >
        </v-card>
        <v-card>
          <v-card-title>Soup</v-card-title>
          <v-card-subtitle>$5</v-card-subtitle>
          <v-img max-height="200px" :src="Soup"></v-img>
          <v-card-text
            >Want something lighter? Have a taste of our soup of the
            day.</v-card-text
          >
        </v-card>
        <v-card>
          <v-card-title>Burger</v-card-title>
          <v-card-subtitle>$8</v-card-subtitle>
          <v-img max-height="200px" :src="Burger"></v-img>
          <v-card-text
            >The all american classic! American cheese on a nice brioche bun
            cooked the way you want.</v-card-text
          >
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>
<script>
import Pizza from "../assets/pizza5.jpg";
import Wings from "../assets/wings.jpg";
import Salad from "../assets/salad.png";
import Soup from "../assets/soup.jpg";
import Sub from "../assets/sub.jpg";
import Burger from "../assets/burger.jpg";

export default {
  name: "ItemMenu",

  data() {
    return {
      Pizza: Pizza,
      Wings: Wings,
      Salad: Salad,
      Soup: Soup,
      Sub: Sub,
      Burger: Burger,
    };
  },
};
</script>
<style lang=""></style>
