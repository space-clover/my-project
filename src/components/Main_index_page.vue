/* eslint-disable */
<template>
    <section class="text-gray-800 w-full">
        <div class="flex flex-col justify-between w-full">
            <div class="w-full flex items-center ">
                <div>
                    <h1 class="text-7xl mb-4 font-bold">{{ consolaActual.nombre }}</h1>
                    <p class="text-md w-2/3 font-semibold">{{ consolaActual.descripcion }}</p>
                    <button class="rounded-lg text-white hover:opacity-80 transition duration-500 bg-red-800 px-2 py-1 font-semibold mt-12"><a :href="consolaActual.enlace" target="_blank">{{ consolaActual.nombre }}</a> </button>
                    
                </div>
                <img :src="consolaActual.img" width="420"  height="80" alt="Imagen de la consola" />
            </div>
            <div class="w-1/4">
            <button class="bg-slate-800 text-white hover:opacity-80 transition duration-500 font-bold rounded-xl p-2" @click="cambiodeconsola()"> cambio de consola</button>
            </div>
        </div>
        <ul class="flex justify-around w-full mt-24">
            <Lista_template title="Free-Shipping" description="llega en 3 dias habiles"/>
            <Lista_template title="Money Guarantee" description="30 dias para recuperar tu dinero"/>
            <Lista_template title="Online Support 24/7" description="puedes llamar cuando necesites"/>
            <Lista_template title="Secure Payment" description="Utilizamos lineas de pago directas con operadores de visa y mastercard"/>
        </ul>
        </section>
        <section class="mt-14">
            <h1 class="text-2xl font-bold text-center py-6 ">Ejercicios 2</h1>
            <div class="flex justify-around">
                <Edad_mayor/>
                <Cinco_nombres/>
                <Seleccion_lista/>
            </div>
        </section>
        <section class="mt-14">
            <h1 class="text-2xl font-bold text-center py-6 ">Ejercicios 3</h1>
            <div class="flex justify-around">
                <Superheroes_poderes/>
                <Futbol_jugadores/>
                <Lenguajes_programacion/>
            </div>
        </section>
    </template>
    
<script>
    import Seleccion_lista from './Seleccion_lista.vue';
    import Cinco_nombres from './Cinco_nombres.vue';
    import Lista_template from './Lista_template.vue';
    import Edad_mayor from './Edad_mayor.vue';
    import Superheroes_poderes from './Superheroes_poderes.vue';
    import Futbol_jugadores from './Futbol_jugadores.vue';
    import Lenguajes_programacion from './Lenguajes_programacion.vue';



    export default {
        components: {
    Lista_template,
    Edad_mayor,
    Cinco_nombres,
    Seleccion_lista,
    Superheroes_poderes,
    Futbol_jugadores,
    Lenguajes_programacion
},
        data() {
        return {
            consolas: [
            {
                nombre: "Nintendo Switch",
                enlace: "https://www.nintendo.com/",
                descripcion:
                "La Nintendo Switch es una consola híbrida que ofrece juegos tanto en modo portátil como en el televisor.",
                img: "https://upload.wikimedia.org/wikipedia/commons/thumb/b/bc/Nintendo-Switch-wJoyCons-BlRd-Standing-FL.png/2560px-Nintendo-Switch-wJoyCons-BlRd-Standing-FL.png",
            },
            {
                nombre: "PlayStation 5",
                enlace: "https://www.playstation.com/",
                descripcion:
                "La PlayStation 5 es la última consola de Sony, conocida por su potencia y gráficos impresionantes.",
                img: "https://buketomnisportpweb.s3.us-east-2.amazonaws.com/products-images/SpOf4P17kxRk8UmdlDz7z2keyrjPrJtjV2noQs7P.jpeg",
            },
            {
                nombre: "Xbox Series X",
                enlace: "https://www.xbox.com/",
                descripcion:
                "La Xbox Series X es la consola de próxima generación de Microsoft, famosa por su rendimiento y biblioteca de juegos.",
                img: "https://timerelojes.com/wp-content/uploads/2022/10/image-44-min.png",
            },
            ],
            consolaActual: {},
            indiceActual: 0,
        };
        },
        mounted() {
        // Mostrar la primera consola al cargar la página
        this.consolaActual = this.consolas[this.indiceActual];
        },
        methods: {
        cambiodeconsola() {
            // Cambiar a la siguiente consola
            this.indiceActual = (this.indiceActual + 1) % this.consolas.length;
            this.consolaActual = this.consolas[this.indiceActual];
        },
        },
    };
    </script>