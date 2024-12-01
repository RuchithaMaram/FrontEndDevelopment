<template>
  <DogHeader/>
  <DogsList :dogsList = dogsList />
</template>

<script>
import DogHeader from "./components/DogHeader.vue";
import DogsList from "./components/DogsList.vue";

  export default{
    name:"App",
    components:{
      DogHeader,
      DogsList
    },
    data(){
      return {
        dogsList:[]
      }
    },methods:{
      async fetchDogsDetails(){
        const res = await fetch("https://dog-collection.onrender.com/api");
        const dogsData = await res.json();
        return dogsData[0].dogs;
      }
    },
    async created(){
      this.dogsList = await this.fetchDogsDetails();
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400..700;1,400..700&display=swap');

  *{
     font-family: "Lora", serif;
  }
</style>