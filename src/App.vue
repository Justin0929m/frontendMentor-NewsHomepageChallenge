<template>
  <div class="desktop-container container">
    <NavBarComp v-if="showComponent"/>
    <NavBarMobile v-if="!showComponent"/>
    <router-view/>
  </div>
</template>

<script>

import NavBarComp from './components/NavBarComp.vue';
import NavBarMobile from './components/NavBarMobile.vue';

export default {
  components: {
    NavBarComp,
    NavBarMobile,
  },
  data() {
    return {
      width: 872,
      showComponent: window.innerWidth >= 872,
    };
  },
  mounted() {
   
    window.addEventListener('resize', this.handleResize);
  },
  beforeDestroy() {
    
    window.removeEventListener('resize', this.handleResize);
  },
  methods: {
    handleResize() {
      
      this.showComponent = window.innerWidth >= this.width;
    },
  },
};

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700;800&display=swap');

:root{

  /* Primary Colours  */

  --softOrange: hsl(35, 77%, 62%);
  --softRed: hsl(5, 85%, 63%);

   /* Neutral Colours */

  --offWhite: hsl(36, 100%, 99%);
  --grayishBlue: hsl(233, 8%, 79%);
  --darkGrayishBlue: hsl(236, 13%, 42%);
  --veryDarkBlue: hsl(240, 100%, 5%);
}

/* CLASSES */

.p-0{
  padding: 0;
}

.m-0{
  margin: 0;
}

body{
  font-family: 'Inter', sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.desktop-container{
  margin: 5rem 10rem;
}

p{
  font-size: 15px;
  color: var(--grayishBlue);
}

@media screen and (width <= 48rem){ 
  .desktop-container{
    margin: 0;
  }

  .container{
    margin-inline: 2rem;
  }
}

</style>