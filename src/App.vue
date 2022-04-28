<script setup>
import Intro from './components/Intro.vue'
import TheWelcome from './components/TheWelcome.vue'
import Research from './components/Research.vue'
import Publications from './components/Publications.vue'
import "bootstrap/dist/css/bootstrap.min.css"
import "bootstrap"
</script>

<template>

  <header>
    <img class="logo" src="./assets/james&cam.jpg" alt="James and Camille 1" width="300" />
    <div class="wrapper">
      <Intro msg="James Conners" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>

  <section >
    <div class="container reveal">

      <Publications />
    </div>
  </section>
</template>
<script type="text/javascript">

function reveal() {
  var reveals = document.querySelectorAll(".reveal");

  for (var i = 0; i < reveals.length; i++) {
    var windowHeight = window.innerHeight;
    var elementTop = reveals[i].getBoundingClientRect().top;
    var elementVisible = 150;

    if (elementTop < windowHeight - elementVisible) {
      reveals[i].classList.add("active");
    } else {
      reveals[i].classList.remove("active");
    }
  }
}

window.addEventListener("scroll", reveal);
</script>


<style>
@import './assets/base.css';
@import url('https://fonts.googleapis.com/css2?family=Asap&display=swap');

#app {
  max-width: 1280px;
  margin: 0 auto;
/*  padding: 2rem;*/

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
    padding-top: 10%;
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

  section{
  min-height: 100vh;
  display: inline-block;
  width: 180%;
  justify-content: center;
  align-items: center;
}
/*section:nth-child(1){
  color: #e0ffff;
  }
section:nth-child(2){
  color: #42455a;
  background: #e0ffff;
} 
section:nth-child(3){
  color: #e0ffff;
}
section:nth-child(4){
  color: #42455a;
  background: #e0ffff;
}*/
section .container{
  margin: 5%;
}
section h1{
  font-size: 3rem;
  margin: 20px;
}
section h2{
  font-size: 40px;
  text-align: center;
}
section .text-container{
   display: flex;
}
section .text-container .text-box{
  margin: 20px;
  padding: 20px;
  background: #00c2cb;
}
section .text-container .text-box h3{
  font-size: 30px;
  text-align: center;
  text-transform: uppercase;
  margin-bottom: 10px;
}

@media (min-width: 1024px){
  section h1{
    font-size: 2rem;
    text-align: center;
  }
  section .text-container{
    flex-direction: column;
  }
}

.reveal{
  position: relative;
  transform: translateY(.75%);
  opacity: 0;
  transition: 1s all ease;
}

.reveal.active{
  transform: translateY(0);
  opacity: 1;
}


}

</style>
