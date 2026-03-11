<template>
    <h3>Css in Vue</h3>
    <p>Styliser un composant avec du css scopé (limité) dans le composant pour eviter des conflits</p>
    <div class="card">
        <h3>Carte stylisée</h3>
        <p>Css scopé in da place</p>
    </div>
</template>

<style scoped>
    .card{
        background-color: darkolivegreen;
        padding: 2rem;
        border-radius: 1rem;
        color: white;
    }
</style>