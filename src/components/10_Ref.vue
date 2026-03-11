<script setup>
import { ref } from 'vue';

const isActive = ref(true);
    const toggle = ()=>{
        isActive.value = !isActive.value;
    }
</script>

<template>
    <h2>Refs</h2>
    <p>Utiliser ref() pour creer des valeurs reactives simple.</p>
    <hr>
    <div>
        <button @click="toggle">{{ isActive ? 'Actif' : 'Inactif' }}</button>
    </div>
</template>