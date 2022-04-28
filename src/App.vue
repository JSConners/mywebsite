<script setup>
import Intro from './components/Intro.vue'
import TheWelcome from './components/TheWelcome.vue'
import Research from './components/Research.vue'
import "bootstrap/dist/css/bootstrap.min.css"
import "bootstrap"
</script>

<template>

  <header>
    <img class="logo" src="./assets/james&cam.png" alt="James and Camille 1" width="300" />
    <div class="wrapper">
      <Intro msg="James Conners" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style>
@import './assets/base.css';

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

header {
  line-height: 1.5;
}

img{
  border-radius: 50%;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
  border: 2px solid #00bd7e;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 2rem 0 0;
  }
}
</style>
