<template>
    <Label>A</Label>
    <input v-model="a"/>

    <Label>B</Label>
    <input v-model="b"/>

    <label>C</label>
    <p>{{ c }}</p>

    <button @click="calculate">Calculate</button>
</template>

<script setup>

import { ref } from 'vue';

const a = ref();
const b = ref();
const c = ref();

const calculate = () => {
    c.value = a.value + b.value;
}

</script>