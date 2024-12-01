<template>
    <div class="dog-container">
        <div class="dog-image">
            <img :src=dog.dog_image alt="Dog Image" class="image"/>
        </div>
         <div>
            <h3>{{dog.dog_name}}</h3>
            <div class="car-details">
                <p><img src="https://img.icons8.com/?size=20&id=87500&format=png&color=000000"/>{{dog.dog_breed}}</p>
                <p>{{dog.dog_color}}</p>
            </div>
            <hr/>
            <div class="dog-details">
                <p><img src="https://img.icons8.com/?size=20&id=117819&format=png&color=000000"/> {{dog.dog_age}}</p>
                <p><img src="https://img.icons8.com/?size=20&id=100637&format=png&color=000000"/> {{dog.dog_life_span}}</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        name:"SingleDog",
        props:{
            dog:Object
        },
    }
</script>

<style>
    .dog-container{
        margin:auto;
        border:transparent;
        border-radius: 10px;
        box-shadow:0 4px 8px 0 rgba(0,0,0,0.2),0 6px 20px 0 rgba(0,0,0,0.19);
        padding:1em;
        margin-bottom: 1em;
    }
    .dog-image img{
        width:100%;
        height:250px;
    }
    .dog-details{
        display: flex;
        justify-content:space-between;
        align-items:center;
    }
    .dog-details img{
        vertical-align:middle;
    }
</style>