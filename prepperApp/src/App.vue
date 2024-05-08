<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import LoginButton from './components/homePage/LoginButton.vue'
import { ref } from 'vue'

const count = ref(0)
</script>

<template>
  <div class="appBody">
    <div class="header">
      <img
        @click="count++"
        alt="Prepper logo"
        class="logo"
        src="@/assets/logo_prepper.svg"
        width="125"
        height="125"
      />
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/login">Login</RouterLink>
    </div>
    <RouterView />
  </div>
</template>

<style scoped>
.header {
  
}
.appBody {
  margin: 1rem;
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
}

.logo {
  margin: 2rem 2rem 0 2rem;
}

nav {
  text-align: left;
  margin-left: -1rem;
  font-size: 1rem;

  padding: 1rem 0;
  margin-top: 1rem;
}
</style>
