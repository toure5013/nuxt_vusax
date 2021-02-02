<template>
  <div>
    <vs-navbar  text-white color="dark" center-collapsed v-model="active">
      <template #left>
        <img src="../assets/logo_orange.png" alt="" class="logo">
      </template>
      <vs-navbar-item  id="guide">
        Home
      </vs-navbar-item>
      <vs-navbar-item  id="docs">
        <NuxtLink to="/">Docs</NuxtLink>
      </vs-navbar-item>
      <template #right>
        <vs-button>Login</vs-button>
        <vs-button>Signup</vs-button>
      </template>
    </vs-navbar>
  </div>
</template>

<script>
export default {
  name: "Appheader",
 data() {
     return {
         active: "guide",
     }
 },
};
</script>

<style>
    .logo{
        width : 15%;
        height : 20%;
    }
</style>
