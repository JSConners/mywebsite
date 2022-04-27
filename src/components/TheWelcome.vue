<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>

  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>About me</template>

    I am a Ph.D. student at Brigham Young University in Computer Science. My lovely wife and I have been married since 2017. Before attending Brigham Young University, I obtained a B.S. in Computer Enigneering Technology (<em> Minors: Electrical Engineering Technology and Computer Science</em>) and a M.S. in Information Technology. 

  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Research</template>

 My area of research is in <em> Usable and Systems Security.</em> I mostly work in authentication (<em>replacing passwords</em>). 
 More about my password replacement research can be found here: <a href="https://letsauth.org" target="_blank">Let's Authenticate</a>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Resume</template>
    This summer I am interning at Sandia National Laboratories in Albuquerque, NM! I will be working with the Center for Cyber Defenders. 
    // You can check out the rest of my resume here: <a href="./../assets/resume.pdf" download="JamesConnersResume.pdf">Resume</a>


  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Socials</template>

    You can find me at:

    <br>
    <div class="center">
   <img alt="twitter logo" src="./../assets/twitter.png" width="20"> &nbsp
   <a target="_blank" href="https://twitter.com/ghostshell1988">@ghostshell1988</a>
   </div>
  </WelcomeItem>
</template>

<style>
@import './../assets/base.css';

  .center {
    display: flex;
    align-items: center;
  }
</style>
