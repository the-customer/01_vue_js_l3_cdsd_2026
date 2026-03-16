<script setup>
import { ref } from 'vue';
import Card from './15_Props.vue';
const products = ref([
    { id: 1, name: 'Stylo', price: 100 },
    { id: 2, name: 'Cahier', price: 100 },
    { id: 3, name: 'Gomme', price: 75 },
    { id: 4, name: 'Crayon', price: 120 },
]);
</script>

<template>
    <h2>15. Props & Validation</h2>
    <p>Les <code>props</code> permettent de passer des donnees du parent vers l'enfant avec validation</p>
    <div class="list">
        <Card v-for="prod in products" :key="prod.id" :product="prod" />
    </div>
</template>

<style scoped>
    .list{
        display: flex;
        gap: 2em;
    }
</style>