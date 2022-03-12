<template lang="">
  <div>
    <v-dialog v-model="dialog" width="1000">
        <template v-slot:activator="{ on, attrs }">
            <v-btn color="secondary" v-on="on" v-bind="attrs">Order</v-btn>
        </template>
        <v-card>
            <v-card-title class="text-h5">Order Form</v-card-title>
            <v-alert v-model="error" color="red" dismissible elevation="4" type="error">{errorMessage}</v-alert>
            <v-form>
                <v-text-field label="Name" v-model="name" v-on="validate()" :error="nameError"></v-text-field>
                <v-text-field label="Phone #" v-model="phone" v-on="validate()" :error="phoneError"></v-text-field>
                <v-text-field label="Address" v-model="address" v-on="validate()" :error="addressError"></v-text-field>
                <v-text-field label="Order" v-model="order" v-on="validate()" :error="orderError"></v-text-field>
                <v-card-actions>
                    <v-btn color="primary" v-on:click="submit()" :loading="loading">Submit</v-btn>
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
          name: "",
          phone: "",
          address: "",
          order: "",

          nameError: false,
          phoneError: false,
          addressError: false,
          orderError: false,

          dialog: false,

          error: false,
          errorMessage: "",
          loading: false,
      }
  },
  methods: {
      async submit() {
          var hasError = false;
          if(this.name == "") { this.nameError = true; hasError = true } else { this.nameError = false }
          if(this.phone == "") { this.phoneError = true; hasError = true } else { this.phoneError = false }
          if(this.address == "") { this.addressError = true; hasError = true } else { this.addressError = false }
          if(this.order == "") { this.orderError = true; hasError = true } else { this.orderError = false }

          if(hasError) { return }

          this.loading = true;
          const worked = await this.sendRequest();
          if(!worked) {
              return
          }
          this.loading = false;

          this.name = ""
          this.phone = ""
          this.address = ""
          this.order = ""

          this.dialog = false;
      },
      validate() {
          if(this.name == "") { this.nameError = true } else { this.nameError = false }
          if(this.phone == "") { this.phoneError = true } else { this.phoneError = false }
          if(this.address == "") { this.addressError = true } else { this.addressError = false }
          if(this.order == "") { this.orderError = true } else { this.orderError = false }
      },
      async sendRequest() {
          const requestOptions = {
              method: 'POST',
              headers: { "Content-Type": "application/json" },
              body: JSON.stringify({name: this.name, phone: this.phone, address: this.address, order: this.order})
          }

          const response = await fetch("http://localhost:8000/order", requestOptions);

          if(response.status == 404) {
              this.error=true;
              return false
          }

          console.log(response)
          return true
      }
  }
};
</script>
<style lang=""></style>
