<script setup>
import { reactive } from 'vue';

const client = reactive({
    fullName:'',
    phone:''
});

const onSubmit = ()=>{
    alert(`Client : ${client.fullName} ${client.phone}`)
}
</script>

<template>
    <section class="card">
        <h2>14. Forms</h2>
        <p>Utiliser <code>v-model</code> pour créer une liaison bidirectionnelle entre les champs de formulaire et les donnees</p>
        <form @submit.prevent="onSubmit">
            <!-- <input @input="(e) => client.fullName = e.target.value" placeholder="Nom complet" type="text" :value="client.fullName"> -->

            <input v-model="client.fullName" placeholder="Nom complet" type="text">
            <input v-model="client.phone" placeholder="Telephone" type="text">
            <button>Valider</button>
        </form>
    </section>
</template>

<style scoped>
    form{ display: flex; gap: 10px; flex-wrap: wrap;}
    input{ padding: 8px; border: 1px solid #ddd; border-radius: 8px; }
    hr{margin-top: 5px;}
</style>