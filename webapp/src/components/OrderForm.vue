<template lang="">
  <div>
    <v-dialog v-model="dialog" width="1000">
        <template v-slot:activator="{ on, attrs }">
            <v-btn color="secondary" v-on="on" v-bind="attrs">Order</v-btn>
        </template>
        <v-card>
            <v-card-title class="text-h5">Order Form</v-card-title>
            <v-form>
                <v-text-field label="Name"></v-text-field>
                    <v-text-field label="Phone #"></v-text-field>
                    <v-text-field label="Address"></v-text-field>
                    <v-text-field label="Order"></v-text-field>
                <v-card-actions>
                    <v-btn color="primary">Submit</v-btn>
                    <v-btn color="secondary" @click="dialog = false">Close</v-btn>
                </v-card-actions>
            </v-form>
        </v-card>
    </v-dialog>
  </div>
</template>
<script>
export default {
  name: "OrderForm",
  data() {
      return {
          dialog: false,
      }
  }
};
</script>
<style lang=""></style>
