<template>
  <div class="about">
    <br>
    <h1 >Personajes Rick and Morty</h1>
    <div class="card-group  justify-content-center">
      <character v-for="character of characters" v-bind:key="character.id" v-bind:character="character"/>
    </div>
  </div>
</template>

<script>

import  axios from  'axios';
import Character from '@/components/Character'
import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap-vue/dist/bootstrap-vue.css';

export default {
  components:{
    Character
  },
  data(){
    return {
      characters: [],
      name:"",
      image:"",
    }
  },
  methods:{
    fetch(){
      console.log("consulata API");
      let result = axios.get("https://rickandmortyapi.com/api/character")
        .then((res) =>{
            console.log(res.data);
            this.characters = res.data.results;
            this.name = res.data.name;
            this.image = res.data.image;
        })
        .catch((err)=> {
            console.log(err)
        })

    }
  },
  created () {
    this.fetch()
  }
}
</script>
<style lang="scss">
  @import 'bootstrap-vue/dist/bootstrap-vue.css';
.about {
  background-color:  rgb(235, 245, 246);
}

</style>

