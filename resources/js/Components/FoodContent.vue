<script setup>
defineProps({
    food: {
        type: Object,
        required: true,
    },
});
</script>

<template>
    <!-- CARD -->
    <div
        class="group w-[317px] hover:scale-105 transition duration-200 ease-in-out"
    >
        <!-- IMAGE -->
        <div class="w-[317px] h-[180px] rounded-t-xl overflow-hidden">
            <img
                :src="`/storage/${food.image} `"
                alt="Menu Food"
                class="object-cover w-full h-full"
            />
        </div>

        <!-- DESC -->
        <div
            class="p-5 px-6 overflow-hidden bg-zinc-200 rounded-b-xl group-hover:bg-red-600 group-hover:text-white transition duration-200 ease-in-out"
        >
            <h1 class="text-[23px] pb-2 font-bold font-raleway">
                {{ food.title }}
            </h1>
            <p class="h-[6rem] tracking-tight" v-html="food.description"></p>

            <h2
                class="font-bold tracking-tight font-montserrat text-xl text-red-600 group-hover:text-white transition duration-200 ease-in-out"
            >
                Rp. {{ food.price }}
            </h2>
        </div>
    </div>
</template>
