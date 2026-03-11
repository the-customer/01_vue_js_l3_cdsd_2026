<script setup>
import { ref } from 'vue';

let count = ref(10);

const increment = () => {
    count.value++;
    
}
</script>
<template>
    <h3>Events</h3>
    <p>Gerer les interactions utilisateurs avec la directive v-on ou son raccourci : @</p>
    <hr>
    <div>
        <span>
            <span>Compteur</span>
            <span>{{ count }}</span>
        </span>
        <!-- <button v-on:click="increment">Incrémenter</button> -->
        <button @click="increment">Incrémenter</button>
    </div>
</template>

<style scoped>
    p{
        display: flex;
        flex-direction: column-reverse;
        justify-content: center;
        align-items: center;
        color: rgb(10,134,176);
    }
    p span{
        font-size: 3rem;
    }

    div p{
        width: 200px;
        height: 200px;
        border-radius: 1rem;
        background-color: lightblue;
        padding: 10px;
    }
    button{
        background-color: #fff;
        color: rgb(10,134,176);
        border-radius: 1rem;
        padding: 15px;
        widows: 200px;
        border: none;
        cursor: pointer;
    }

    div{
        widows: 400px;
        height: 400px;
        border-radius: 1rem;
        background-color: rgb(10,134,176);
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        gap: 1rem;
    }
</style>