<script setup>
    import { RouterLink } from 'vue-router'
</script>

<template>
    <header class="bg-wa-dark py-2 px-3 flex justify-between items-center text-white fixed w-full">
        <div class="flex items-center">
            <RouterLink to="/">
                <i class="fas fa-arrow-left"></i>
            </RouterLink>
            <img class="w-12 h-12 rounded-full mx-2" src="https://via.placeholder.com/150" alt="">
            <div class="">
                <h5 class="text-lg font-semibold">Belan</h5>
                <p class="text-sm">Alice, Francis, Jack, Ned, Peter</p>
            </div>
        </div>

        <div class="space-x-2">
            <span class="material-icons transform -rotate-45">attach_file</span>
            <span class="material-icons">more_vert</span>
        </div>
    </header>
</template>