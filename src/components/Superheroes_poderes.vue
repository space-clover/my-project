<template>
        <div class=" text-center">
        <h2 class="text-xl text-red-900">Superhéroes y sus superpoderes:</h2>
        <ul>
            <li v-for="(superheroe, poder) in superheroes" :key="poder">
            {{ superheroe }} - {{ poder }}
            </li>
        </ul>
        </div>
</template>
    
<script>
    export default {
        data() {
        return {
            superheroes: {
            "Superman": "Super fuerza",
            "Spider-Man": "Telarañas",
            "Wonder Woman": "Lazo de la verdad",
            "Batman": "Inteligencia",
            "Flash": "Velocidad"
            }
        };
        }
    };
</script>