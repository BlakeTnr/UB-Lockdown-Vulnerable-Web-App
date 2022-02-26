<template>
  <v-app>
    <v-app-bar app dark>
      <v-row>
        <v-col md="2">
          <v-app-bar-title> Vinney's Pizzzzzariaa </v-app-bar-title>
        </v-col>
        <v-spacer />
        <v-col md="1">
          <HoursButton />
        </v-col>
        <v-col md="1">
          <OrderForm />
        </v-col>
      </v-row>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import HoursButton from "./components/HoursButton.vue";
import OrderForm from "./components/OrderForm.vue";

export default {
  name: "App",

  components: {
    HoursButton,
    OrderForm,
  },
};
</script>
