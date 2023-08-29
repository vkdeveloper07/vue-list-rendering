<template>
    <h2>Normal</h2>
    <div class="container">
        <p>Books</p>
        <ul>
            <li v-for="book in books" :key="book.id">{{ book.name }}</li>
        </ul>
    </div>
    <br>
    <h2>With index</h2>
    <div class="container">
        <ul v-for="(student, index) in students">
            <li>{{ index }} - {{ student.name }}</li>
        </ul>
    </div>
    <br>
    <h2>With destructuring</h2>
    <div class="container">
        <ul v-for="{ name } in students">
            <li>{{ name }}</li>
        </ul>
    </div>

    <br>
    <h2>With Array</h2> 
    <div class="container">
        <ul>
            <li v-for="car in cars">
                {{ car }}</li>
        </ul>
    </div>

    <br>
    <h2>With Range ('n' starts with 1 instead of 0)</h2>
    <div class="container">
        <ul>
            <li v-for="n in 10">
                {{ n }}</li>
        </ul>
    </div>
    
</template>

<script setup>
import { ref } from 'vue';
let books = ref([
    { id: 1, name: 'Atomic habits' },
    { id: 2, name: 'Rich dad Poor dad' },
    { id: 3, name: 'Ikigai' },
])

let students = ref([
    { id: 1, name: 'Jk' },
    { id: 2, name: 'Paul' },
    { id: 3, name: 'John' },
])

let cars = ref(['Audi', 'BMW', 'Toyota'])
</script>

<style scoped>
.container {
    width: 100%;
    border: 1px solid white;
}
</style>