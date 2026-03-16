<script setup>
defineProps({
    // product: Object
    product:{
        type: Object,
        required: true,
        validator(value){
            //Validation metier
            return (value &&
                typeof value.id === 'number' &&
                typeof value.name === 'string' &&
                typeof value.price === 'number' &&
                value.price > 0
            )
        }
    }
})
</script>


<template>
    <article class="card">
        <h3>{{ product.name }}</h3>
        <p class="meta">{{ product.price }} CFA</p>
        <p class="meta"> {{ product.id }}</p>
    </article>
</template>

<style scoped>
    .name{ margin: 0; font-size: 16px; }
    .price{ margin: 6px 0 0; font-weight: 700; }
    .meta{ margin: 0; font-size: 16px; color: #666; }
    article{ border: 1px solid white }
</style>