<template>
  <div>
    <h1>Witaj w systemie do zapisow na zajecia </h1>
    <div v-if= "authenticated">
    <h3>Zalogowany jako {{ email}}</h3>
    <a @click="logOut()">Wyloguj</a>
  </div>
<div v-else>
Zaloguj sie:
<input type="text" v-model="email">
<button @click="logIn()"> Zaloguj sie</button>
</div>
</div>
</template>

<script>
import"milligram";

export default {
    data() {
     return {
        authenticated: false,
        email: ""
      };
   },
  methods: {
    logIn() {
      this.authenticated=true;
     },
  logOut(){
    this.authenticated=false;
    this.email="";
  }
  }
};


</script>

<style>
a {
  color: blue;
}
</style>


