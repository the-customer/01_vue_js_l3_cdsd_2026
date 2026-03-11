<script setup>
import { reactive } from 'vue';
    const names = ['Breukh','Toto','Tata','Titi']
    // const user = {
    //     nom: 'Breukh',
    //     age: 20,
    //     email: 'breukh@example.com',
    //     ville: 'BreukhVille'
    // }

    const user = reactive({
        nom: names[0],
        age: 20,
        email: 'breukh@example.com',
        ville: 'BreukhVille'
    });

    const getRandomName = () => {
        const i = Math.floor(Math.random() * names.length)
        console.log(i)
        user.nom = names[i];
    }
</script>

<template>
    <h3>Reactive</h3>
    <p>Utilser lorsqu'on a des object dont le changement avec le rendu</p>
    <hr>
    <div>
        <h3>{{user.nom}}</h3>
        <span>Age : {{ user.age }}</span>
        <span>Email : {{user.email}}</span>
        <span>Ville : {{user.ville}}</span>
    </div>
    <hr>
    <button @click="getRandomName">Randome Name</button>
</template>

<style scoped>
div{
    display: flex;
    flex-direction: column;
}
</style>