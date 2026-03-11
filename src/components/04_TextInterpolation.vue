<script setup> 
    const name = "Toto";
    const age = 18;
    const address = "Toto ville"
    const person = {
        name : 'Titi',
        age : 10,
        address: 'Titi Town'
    }
</script>
<template>
    <div>
        <h3>String Interpolation:</h3>
        <p>Permet d'afficher le contenu de variable (ou constant, objet) dans le template</p>
        <hr>
        <p>Bonjour, je m'appelle {{ person.name }}</p>
        <p>J'ai {{person.age}} ans</p>
        <p>J'habite à {{person.address}}</p>
    </div>
</template>

<style scoped>
    div{
        border: 1px solid lightgreen;
        padding: 10px;
    }
</style>