<template>
  <v-app>    
    <Navbar />
    <v-main>
      <v-img src="./assets/pexels-kai-pilger-996329.jpg" height="85vh" gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)">
        <v-container class="white--text text-center" id="header">
          <h1 id="main">Rhyme International Limited</h1>
          <v-subtitle>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Et architecto magnam autem, rerum impedit quisquam ipsam illo earum quis beatae doloribus dolorum aliquam veniam enim vero dicta consequatur. Possimus, repellat?</v-subtitle><br>
          <v-btn flat large class="text-center my-4"><b>Contact Us</b></v-btn>
        </v-container>
      </v-img>
      <About />
      <Contact />
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar'
import About from './components/About'
import Contact from './components/Contact'
import Footer from './components/Footer'

export default {
  name: 'App',

  components: {
    Navbar,
    About,    
    Contact,
    Footer,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
#main{
  padding-top: 16vh;
}

*{
  scroll-behavior: smooth;
}

#header{
  width: 70%;
}
</style>