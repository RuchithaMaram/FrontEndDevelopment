<template>
    <div class="grid-container">
        <div v-for="dog of dogsList" :key="dog.dog_id">
            <SingleDog :dog = dog />
        </div>
    </div>
</template>

<script>
    import SingleDog from "./SingleDog.vue";

    export default{
        name:"DogsList",
        components:{
           SingleDog
        },
        props:{
            dogsList: Array
        }
    }
</script>

<style scoped>
    .grid-container{
        display: grid;
        grid-template-columns: auto auto auto;
        gap:2em;
        width:80%;
        margin:auto;
    }
</style>