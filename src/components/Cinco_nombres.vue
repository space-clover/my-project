<template>
    <div >
        <div class="flex ">
            <div class="flex flex-col">
            <input class="p-1" v-model="usuario" type="text" placeholder="Usuario">
            <input class="p-1" v-model="contrasena" type="password" placeholder="Contraseña">
        </div>
        <button class= "ml-4  bg-slate-200 rounded-xl px-2 transition duration-500 hover:opacity-80" @click="verificarCredenciales">Iniciar Sesión</button>
        </div>
        <ul v-if="credencialesValidas">
            <li class="font-bold text-lg text-green-800" v-for="(nombre, index) in nombres" :key="index">{{ nombre }}</li>
        </ul>
    </div>
</template>

<script>
    export default {
        data() {
        return {
            usuario: "",
            contrasena: "",
            credencialesValidas: false,
            nombres: ["Gerardo", "Rigoberto", "Pomelo", "Manzano", "alfredo"]
        };
        },
        methods: {
        verificarCredenciales() {
            if (this.usuario === "adminItca" && this.contrasena === "Itca123!") {
            this.credencialesValidas = true;
            } else {
            this.credencialesValidas = false;
            }
        }
        }
    };
</script>