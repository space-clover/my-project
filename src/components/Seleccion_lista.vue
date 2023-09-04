<template>
    <div class="text-black">
        <select class="p-1 border border-slate-900 rounded-xl  " v-model="categoriaSeleccionada " >
            <option  value="A">Categoría A</option>
            <option value="B">Categoría B</option>
            <option value="C">Categoría C</option>
        </select>
        <button class= "ml-4  bg-slate-200 rounded-xl px-2 transition duration-500 hover:opacity-80 py-2" @click="mostrarProductos">Mostrar Productos</button>
        <ul>
            <li class="font-bold text-lg text-green-800" v-for="(producto, index) in productosFiltrados" :key="index">{{ producto }}</li>
        </ul>
        </div>
</template>
    
<script>
    export default {
        data() {
        return {
            categoriaSeleccionada: "",
            productos: {
            A: ["Producto1A", "Producto2A", "Producto3A"],
            B: ["Producto1B", "Producto2B", "Producto3B"],
            C: ["Producto1C", "Producto2C", "Producto3C"]
            },
            productosFiltrados: []
        };
        },
        methods: {
        mostrarProductos() {
            this.productosFiltrados = this.productos[this.categoriaSeleccionada] || [];
        }
        }
    };
</script>