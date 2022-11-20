<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <img alt="Site logo" class="logo" src="@/assets/erisu.jpg" width="125" height="125" oncontextmenu="return false;"/>

    <div class="wrapper">
      <HelloWorld msg="ようこそ！Johmaruのサイトへ" />
      
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/profile">Profile</RouterLink>
      </nav>
      <a href="https://github.com/johmaru/JohmaruWebSite/tree/master" class="GitBTN" target="_blank"><img src="@/assets/Octocat.png" alt="GitPage" width="128" height="128" oncontextmenu="return false;"></a>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1%;
  max-height: 100%;
}

.logo {
  display: block;
  position: fixed;
  top: 2rem;
  left: 0rem;
}

.GitBTN{
  bottom: 0.5rem;
  right: 0rem;
  position: fixed;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  left: 25rem;
  top: -1rem;
  position: fixed;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {

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
