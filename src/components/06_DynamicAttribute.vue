<script setup>
const attributeName = "title";
const attributeValue = "Survolez-moi"
</script>

<template>
    <h3>Dynamic Attribute</h3>
    <p>Utiliser des noms d'attributs dynamiques pour creer des composants flexibles</p>
    <hr>
    <input :[attributeName]="attributeValue">
    <button title="button ok">ok</button>
</template>