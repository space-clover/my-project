<template>
        <div>
        <h2>Jugadores de fútbol:</h2>
        <ul>
            <li v-for="(jugador, index) in jugadores" :key="index">
            Nombre: {{ jugador.nombre }} - Equipo: {{ jugador.equipo }}
            </li>
        </ul>
        </div>
    </template>
    
<script>
    export default {
    data() {
    return {
        jugadores: [
            { nombre: "Lionel Messi", equipo: "Paris Saint-Germain" },
            { nombre: "Cristiano Ronaldo", equipo: "Manchester United" },
            { nombre: "Neymar Jr.", equipo: "Paris Saint-Germain" },
            { nombre: "Kylian Mbappé", equipo: "Paris Saint-Germain" },
            { nombre: "Sergio Ramos", equipo: "Paris Saint-Germain" },
            { nombre: "Luka Modric", equipo: "Real Madrid" },
            { nombre: "Mohamed Salah", equipo: "Liverpool" },
            { nombre: "Robert Lewandowski", equipo: "Bayern Munich" },
            { nombre: "Kevin De Bruyne", equipo: "Manchester City" },
            { nombre: "Harry Kane", equipo: "Tottenham Hotspur" }
        ]
    };
}
};
  </script>