<script setup>
import { ref } from 'vue';

const isVisible = ref(false);
const type = ref('info');
</script>
<template>
    <h1 v-if="1==1">{{ type }}</h1>
    <p>Utiliser <code>v-if</code>, <code>v-else</code>, <code>v-else-if</code>, <code>v-show</code> pour afficher conditionnellement des elements</p>
        <div v-if="isVisible" class="screen">
            <p v-show="type=='info'" class="info">Info</p>
            <p v-show="type=='success'" class="success">Success</p>
            <p v-show="type=='error'" class="error">Error</p>
        </div>
        <button @click="isVisible = !isVisible" class="main">Afficher/Cacher</button>
        <button @click="type='success'" class="success">Success</button>
        <button @click="type='error'" class="error">Error</button>
        <button @click="type='info'" class="info">Info</button>
</template>

<style scoped>
    .screen{
        width: 180px;
        padding: 20px 0;
        text-align: center;
    }
    button.main{
        display: block;
        width: 180px;
        background-color: #fff;
        color: gray;
        border: 2px solid gray;
        margin-bottom: 1rem;
    }
    .error{
        background-color: #fff;
        color: rgb(215, 89, 89);
        border: 2px solid rgb(215, 89, 89);
    }
    .info{
        background-color: #fff;
        color: cornflowerblue;
        border: 2px solid cornflowerblue;
    }
    .success{
        background-color: #fff;
        color: rgb(66, 145, 66);
        border: 2px solid rgb(66, 145, 66);
    }
    button{
        outline: none;
        padding: 8px 0;
        width: 60px;
        cursor: pointer;
    }
</style>