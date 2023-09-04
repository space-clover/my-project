/* eslint-disable */
<template>
    <li class="flex p-2 justify-around w-1/4">
        <div class="flex-col justify-center transition-transform hover:translate-y-[-5px] hover:opacity-80">
            <h1 class="text-lg font-bold">{{ title }}</h1>
            <h1 class="text-sm font-extralight text-gray-700">{{ description }}</h1>
        </div>
    </li>
</template>

<script>
    export default {
        props: {
        title: {
            type: String,
            required: true,
        },
        description: {
            type: String,
            required: true,
        },
        },
    };
</script>