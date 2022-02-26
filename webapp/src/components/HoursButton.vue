<template lang="">
    <v-dialog v-model="dialog" width="500" >
        <template v-slot:activator="{ on, attrs }">
            <div>
                <v-btn color="secondary" v-bind="attrs" v-on="on">Hours</v-btn>
            </div>
        </template>
        <v-card>
            <v-card-title class="text-h5">Hours</v-card-title>
            <v-card-text>Monday-Friday: 8am-5pm</v-card-text>
            <v-card-text>Satuday and Sunday: 9am-2pm</v-card-text>
            <v-card-actions>
                <v-btn color="primary" @click="dialog = false">Close</v-btn>
            </v-card-actions>
        </v-card>
    </v-dialog>
</template>
<script>
export default {
  name: "HoursButton",

  data() {
    return {
        dialog: false,
    };
  },
};
</script>
<style lang=""></style>
