<script setup>
    defineProps({
        chat: {
            type: Object,
            required: true
        }
    })
</script>

<template>
    <section class="m-2 flex">
        <div class="w-2/12 py-2">
            <img class="w-12 h-12 rounded-full" :src="chat.image" alt="">
        </div>
        <article class="w-10/12 border-b-2 border-gray-100 py-2">
            <div class="flex justify-between">
                <h2 class="font-semibold">{{ chat.name }}</h2>
                <p class="text-green-500">{{ chat.time }}</p>
            </div>
            <div class="flex justify-between">
                <h2 class="text-sm" :class="chat.count > 0 ? 'text-green-500':'text-gray-500'">{{ chat.message }}</h2>
                <p v-if="chat.count > 0" class="bg-green-500 text-white w-5 h-5 rounded-full text-center text-sm">
                    {{ chat.count }}
                </p>
            </div>
        </article>
    </section>
</template>