<template>
  <div id="app">
    <nav class="rounded-bottom justify-content-center">
      <b-row class="d-flex flex-row" >
        <b-col md="1" class=" d-flex text-center  flex-column">
        </b-col>
        <b-col md="2" >
          <img alt="logo" src="./assets/Rickandmorty.png" style="width: 150%">
        </b-col>
        <b-col md="6" class=" d-flex text-center  flex-column">
        </b-col>
        <b-col md="3" class=" d-flex text-center  flex-column justify-content-center">
          <div class="d-flex flex-row justify-content-center">
            <router-link to="/">Sobre</router-link> 
            <router-link to="/about">Personajes </router-link>
          </div>
        </b-col>
      </b-row>
    </nav>
    <router-view/>

    <footer>
      <b-row class="d-flex flex-row" >
        <b-col md="4" class=" d-flex text-center  flex-column">
        </b-col>
        <b-col md="4" class=" d-flex text-center  flex-column"> 
          <a class="mb-1" href="https://www.linkedin.com/in/juanstevensanchezcastro-desarrolladorfrontend/" target="_blank">
          <i class="fab fa-linkedin"></i>
            &nbsp;Juan Steven Sanchez Castro
          </a>
          <p class="mb-0">
            <i class="fas fa-phone"></i>&nbsp;+57 312 205 70 69
          </p>
          <p class="mb-0">
            <i class="fas fa-envelope"></i> &nbsp;steven.jssc@gmail.com
          </p>
        </b-col>
        <b-col md="4" class=" d-flex text-center  flex-column">
        </b-col>         
      </b-row>      
    </footer>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-family: 'Pacifico', cursive;
  font-family: 'Lobster', cursive;
  font-family: 'Dancing Script', cursive;
  text-align: center;
  color: #2c3e50;
  //background-image: url('./assets/fondo.png');
}
nav {
  padding: 30px;
  background-color:  rgb(1, 177, 200);
  background-image: linear-gradient(to left,rgb(3, 63, 71),rgb(6, 113, 128));
  background-image: rgb(1, 177, 200);
  //background-image: url('./assets/fondo.png');
  a {
    font-weight: bold;
    color: rgb(0, 178, 202);
    padding: 20px;    
    &.router-link-exact-active {
      color: rgb(255, 255, 255);
    }
  }
}
footer {
  padding: 15px;
  background-color:  rgb(1, 177, 200);
  background-image: linear-gradient(to left,rgb(3, 63, 71),rgb(6, 113, 128));
  background-image: rgb(1, 177, 200);
  //background-image: url('./assets/fondo.png');
  a { 
    color: rgb(255, 255, 255);     
    }
  p {  
    color: rgb(255, 255, 255); 
  }
}
</style>
