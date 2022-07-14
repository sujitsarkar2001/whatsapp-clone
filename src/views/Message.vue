<script setup>
import { reactive } from "vue";
import MessageHeader from "@/components/messages/Header.vue";

const chats = reactive([
  {
    name: "Francis Whitmans",
    message: "😜😝 Anyone who want to tag alone is more than welcome",
    time: "11:39 AM",
  },
  {
    name: "you",
    message: "🚤🏊🏄⛵🚣🌅💭",
    time: "11:42 AM",
  },
]);
</script>

<template>
    <MessageHeader />

    <section
        class="h-screen py-24 bg-[url('./src/assets/whatsapp_background.png')]"
    >
        <article
            v-for="(chat, key) in chats"
            :key="key"
            class="px-3 py-1 flex"
            :class="chat.name == 'you' ? 'justify-end' : ''"
        >
            <div class="px-3 rounded w-9/12 relative" :class="chat.name == 'you' ? 'bg-[#e3fbcc]' : 'bg-white'">
                <span
                class="material-icons text-5xl absolute top-0"
                :class="chat.name == 'you' ? 'right-0 -mt-5 -mr-6 text-[#e3fbcc]' : 'left-0 -mt-5 -ml-6 text-white'"
                >arrow_drop_down</span
                >
                <h1 class="text-red-500">{{ chat.name }}</h1>
                <div>
                    <p>{{ chat.message }}</p>
                    <p class="text-sm text-gray-400 text-right">{{ chat.time }}</p>
                </div>
            </div>
        </article>
    </section>
</template>
