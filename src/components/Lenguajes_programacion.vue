<template>
        <div>
        <h2>Lenguajes de programación populares:</h2>
        <ul>
            <div class="bg-programaciondiv text-center rounded-lg font-bold text-red-950 py-2 my-2" v-for="(lenguaje, index) in lenguajes" :key="index">
            {{ lenguaje }}
            </div>
        </ul>
        </div>
</template>

<script>
    export default {
        data() {
        return {
            lenguajes: ["JavaScript", "Python", "Java", "C#", "Ruby"]
        };
        }
    };
</script>
