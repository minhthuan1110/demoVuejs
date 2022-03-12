<template>
  <div id="app" @scroll="handleScroll">
   <Header/>
   <div class="container">
     <Container1/>
     <Container2/>
     <Container3/>
     <Container4/>
   </div>
   <Footer/>
   <div class="btn-backgotop " @click="goTop">
     <i class="fa-solid fa-chevron-up"></i>
   </div>
  </div>
</template>

<script>

import Header from './components/header/Header.vue'
import Footer from './components/footer/Footer'
import Container1 from './components/container/Container1'
import Container2 from './components/container/Container2.vue'
import Container3 from './components/container/Container3'
import Container4 from './components/container/Container4'


export default {
  name: 'App',
  components: {
    Header,
    Container1,
    Container2,
    Container3,
    Container4,
    Footer
  },
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll () {
      let btnBackTop = document.querySelector('.btn-backgotop');

      if (window.scrollY > 150) {
         btnBackTop.classList.add("active");
      }
      else { 
         btnBackTop.classList.remove("active");
      }
    },
    goTop: function() {
      document.body.scrollTop = 0;
      document.documentElement.scrollTop = 0;
    }
  }
}
</script>

<style  >
   body {
    margin: 0;
    padding: 0;
  }
  .container {
    width:100%;
    height:auto;
    margin:70px 0 40px 0;
  }
  .btn-backgotop {
    display: none;
    position: fixed;
    right:5%;
    bottom: 5%;
    width : 45px;
    height: 45px;
    text-align: center;
    background-color:#fff;
    border-radius:5px ;
    box-shadow: 0 0 3px .6px rgba(163, 151, 151, 0.452);
    z-index: 10000;

    
  }

  .btn-backgotop i{
        line-height:45px;
        color:#878787;
    }
  .btn-backgotop.active {
    display:block;
  }
</style>
