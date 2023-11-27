<template>
  
    <div >
        <div class="card mt-4 me-4 ms-4">            
            <img v-bind:src="character.image"  alt="character"  class="rounded">
            <div class="card-body">
                <h5>{{ character.name }}</h5>              
                <b-button @click="modalshow(character)" class="boton">Más información</b-button>            
            </div>
        </div>

        <b-modal v-model="modalShow" :title="name" size="sm"  hide-footer >
            <div  class="fondomodal" > 
                <div class="rounded card-group  justify-content-center ">
                    <img v-bind:src="character.image"  alt="character" class="rounded mt-3"  style="width: 90%"  >
                </div>
                <br>
                <div class="d-flex align-items-end">
                    <h5 class="mr-3 mb-0">  Nombre:  &nbsp; </h5> 
                    <p class="mb-0">{{ name }}</p>
                </div>
                <div class="d-flex align-items-end">
                    <h5 class="mr-3 mb-0">  Genero:  &nbsp; </h5> 
                    <p class="mb-0">{{ gender }}</p>
                </div>
                <div class="d-flex align-items-end">
                    <h5 class="mr-3 mb-0">  Estatus:  &nbsp; </h5> 
                    <p class="mb-0">{{ status }}</p>
                </div>
                <div class="d-flex align-items-end">
                    <h5 class="mr-3 mb-0"> Especie:  &nbsp; </h5> 
                    <p class="mb-0">{{ species }}</p>
                </div>
            </div>
           
        </b-modal>       

    </div>

</template>

<script>
export default {
    data() {
      return {
        modalShow: false,
        gender: "",
        name: "",
        species: "",
        status: "",
        }
    },
    methods: {
        modalshow(character){
        this.modalShow = true;
        this.gender=this.character.gender;
        this.name=this.character.name;
        this.species=this.character.species;
        this.status=this.character.status;
        }
    },
    props: ["character"]
};

</script>

<style lang="scss">
.fondomodal {
  background-color:  rgb(235, 245, 246);
  font-family: 'Dancing Script', cursive;
  //background-image: url('../assets/centro.png');
}
.boton {
  text-align: center;
  color: rgb(255, 255, 255);
  background-color: rgb(6, 113, 128);
}

</style>
