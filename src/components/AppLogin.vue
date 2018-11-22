<template>
<v-container>
  <v-alert
      :value="alert"
      type="warning"
      color="red"
    >
      Enter email and passsword
    </v-alert>
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
      alert: false
      
    };
  },
  methods:{
      submit(){
        if(!this.email && !this.password)
          // console.log(`Email is ${this.email}, password is ${this.password}`);
          this.alert=true;
      }
  }
};
</script>


