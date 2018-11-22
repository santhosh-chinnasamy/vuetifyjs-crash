<template>
<v-container>
    <v-form @submit.prevent="submit">
    <v-text-field
      v-model="email"
      label="E-mail"
      required
    ></v-text-field>

    <v-text-field
    v-model="password"
     type="password"
      label="Password"
      required
    ></v-text-field>
    <v-btn class="green" type="submit">Login</v-btn>
  </v-form>
</v-container>
  
</template>

<script>
export default {
  data() {
    return {
      email: null,
      password: null,
      
    };
  },
  methods:{
      submit(){
          console.log(`Email is ${this.email}, password is ${this.password}`);
      }
  }
};
</script>


