

<template>
  <div>
    <h3>Hello world, this my first app</h3>
    <p>Un composant une partie reutilisable et une sorte de balise qui vient avec son propre html, js et css. Il doit au minimum avoir la balise script ou template</p>
    <p>Mettre l'attibut <code>scoped</code> au niveau de la balise <code>style</code> pour limiter le css dans le composant</p>
  </div>
</template>

<style scoped>
  h3{
    color:darkred;
  }
  p{
    color: lightblue;
  }
</style>
