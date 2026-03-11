<script setup>
import { computed, ref } from 'vue';

    const firstname = ref("Breukh")
    const lastname = ref("Ndiaye")

    const fullname = computed(()=>{
        return `${firstname.value} ${lastname.value}`
    })
</script>
<template>
    <h3>Computed</h3>
    <p>Les proprietes calculees sont mise en cache et recalculees uniquement lorsque leur dependences changes</p>
    <hr>
    <div>
        <h3>{{fullname}}</h3>
        <form>
            <input type="text" :value="firstname">
            <input type="text" :value="lastname">
        </form>
    </div>
</template>
<style scoped>
    input{
        display: block;
        padding: 5px;
        font-size: 18px;
        margin-bottom: 1rem;
        color: whitesmoke;
        opacity: 0.5;
    }
</style>