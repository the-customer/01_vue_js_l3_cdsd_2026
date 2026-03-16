<script setup>
import { ref } from 'vue';

const products = ref([
    { id:1, name: 'Stylo', price: 100 },
    { id:2, name: 'Cahier', price: 500 },
    { id:3, name: 'Gomme', price: 75 },
    { id:4, name: 'Crayon', price: 120 },
]);
const remove = (id) => {
    products.value = products.value.filter(p => p.id !== id);
}
</script>

<template>
    <section class="card">
        <h2>13. List</h2>
        <p>Utiliser le <code>v-for</code> pour parcourir des tableaux et afficher des listes d'elements</p>
        <ul>
            <li v-for="product in products" :key="product.id">
                {{ product.name }} - {{ product.price }} FCFA
                <button @click="remove(product.id)"> ❌ </button>
            </li>
        </ul>
    </section>
</template>

<style scoped>
    .card{
        padding: 16px;
        border: 1px solid #eee;
        border-radius: 12px;
    }
    li{
        display: flex;
        justify-content: space-between;
        width: 250px;
    }
    button{
        border: none;
        background: none;
        cursor: pointer;
    }
</style>