<template>
    <Label>A</Label>
    <input v-model="a"/>

    <Label>B</Label>
    <input v-model="b"/>

    <label>C</label>
    <p>{{ c }}</p>

    <label>Opération</label>
    <select v-model="operator">
        <option value="+">+</option>
        <option value="-">-</option>
        <option value="*">*</option>
        <option value="/">/</option>
    </select>

    <button @click="calculate">Calculate</button>
</template>

<script setup>

import { ref } from 'vue';

const a = ref();
const b = ref();
const c = ref();

const operator = ref();

const calculate = () => {
    switch(operator.value) {
        case "+": 
            c.value = a.value + b.value;
            break;
        case "+": 
            c.value = a.value - b.value;
            break;
        case "*":
            c.value = a.value * b.value;
            break;
        case "/":
            c.value = a.value / b.value;
            break;
    }
}

</script>