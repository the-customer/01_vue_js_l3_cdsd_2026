<template>
    <div>
        <h3>V-BIND</h3>
        <p>Lier dynamiquement des attributs html aux donnees avec v-bind</p>
        <hr>
        <!-- <input :type="inputType" v-bind:value="text"> -->
        <input :type="inputType" :value="text">
        <button :disabled="isDisabled">Cliquez-moi</button>
    </div>
</template>


<script setup>
    const inputType = "text"
    const text = "Un exemple";
    const isDisabled = true;
</script>


<style scoped>
    input{
        padding: 5px;
        outline: none;
    }
</style>