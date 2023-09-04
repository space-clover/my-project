<template>
    <div>
      <input v-model="edad" type="number" class="rounded-lg border bg-slate-200 mr-2 p-1" placeholder="Ingresa tu edad">
      <button  @click="verificarEdad">Verificar Edad</button>
      <p class="font-bold text-red-700" v-if="esMenorDeEdad">Es menor de edad</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
        return {
        edad: 0,
        esMenorDeEdad: false
    };
    },
    methods: {
        verificarEdad() {
            if (this.edad < 18) {
            this.esMenorDeEdad = true;
            } else {
            this.esMenorDeEdad = false;
            }
        }
        }
  };
  </script>
  