<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<template>
  <header>
    <img alt="Simple Logo" class="logo" src="" width="125" height="125" />
    <nav>
        <router-link to="/" exact>Home</router-link>
        <router-link to="/about">About</router-link>
        <!--Add the RouterLink component to the template -->
    </nav>
    <div class="wrapper">
      <h1 class="homeTitle">Simple Blog</h1>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
.homeTitle {
  color: rgb(3, 3, 4);
  text-align: center;
  margin: 0;
  font-size: 3.6rem;
}

header {
  line-height: 1.5;
  max-height: 100vh;
  color: rgb(3, 3, 4)
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
