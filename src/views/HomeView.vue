<template>
<div class="carta">
      <b-row>
          <b-col md="3" class=" d-flex text-center  flex-column">
            <img alt="Rick" src="../assets/Rick.png" class="img-fluid" >
          </b-col>          
          <b-col md="6" class="mt-1 d-flex flex-column justify-content-center">           
            <h1 class="mt-4 my-1">Rick and Morty</h1>            
            <p class="mt-4 my-4 texto">
              Rick and Morty es una serie de televisión estadounidense
              de animación para adultos creada por Justin Roiland y Dan Harmon en 2013 para 
              Adult Swim, también se emitió en Cartoon Network. La serie sigue las desventuras
              de un científico, Rick Sánchez, y su fácilmente influenciable nieto, Morty,
              quienes pasan el tiempo entre la vida doméstica y los viajes espaciales,
              temporales e intergalácticos. Dan Harmon, el cocreador de la serie y 
              Justin Roiland son los encargados de las voces principales de Morty y Rick,
              la serie también incluye las voces de Chris Parnell, Spencer Grammer y 
              Sarah Chalke.            
            </p>
            <br>
            <div class="d-flex justify-content-center">
              <img class="img-fluid" alt="Centro" src="../assets/centro1.png" style="width: 65%;">
            </div>   
          </b-col>    
          <b-col md="3"  class=" d-flex text-center  flex-column"> 
            <img alt="Morty" src="../assets/Morty.png"  class="img-fluid" >   
          </b-col> 
        </b-row>    
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; 

@Component({
  components: {
    HelloWorld,
  },
})
export default class HomeView extends Vue {}
</script>
