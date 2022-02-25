<template>
  <v-app>
    <v-app-bar
      app
      dark
    >

    <v-row>
      <v-col md='2'>
        <v-app-bar-title>
          Vinney's Pizzzzzariaa
        </v-app-bar-title>
      </v-col>
      <v-spacer/>
      <v-col md='1'>
        <v-btn color='secondary'>
          Home
        </v-btn>
      </v-col>
      <v-col md='1'>
        <v-btn color='secondary'>
          Hours
        </v-btn>
      </v-col>
      <v-col md='1'>
        <v-btn color='secondary'>
          Order
        </v-btn>
      </v-col>
    </v-row>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
