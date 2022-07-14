<script setup>
import { RouterLink } from 'vue-router'
import ChatHeader from "@/components/chat/Header.vue";
import ChatList from "@/components/chat/List.vue";

import { reactive } from "vue";

const chats = reactive([
  {
    image: "https://via.placeholder.com/150",
    name: "Whitemans Chat",
    message: "Ned: Yeah I think I know wha...",
    time: "11:45 AM",
    count: 3,
  },
  {
    image: "https://via.placeholder.com/150",
    name: "Stewart Family",
    message: "Steve: Great, thanks!",
    time: "11:39 AM",
    count: 1,
  },
  {
    image: "https://via.placeholder.com/150",
    name: "Alice Whitman",
    message: "Image",
    time: "YESTERDAY",
    count: 0,
  },
  {
    image: "https://via.placeholder.com/150",
    name: "Jack Whitman",
    message: "0:07",
    time: "FRIDAY",
    count: 0,
  },
  {
    image: "https://via.placeholder.com/150",
    name: "Lunch Group",
    message: "You: Sounds good!",
    time: "FRIDAY",
    count: 0,
  },
  {
    image: "https://via.placeholder.com/150",
    name: "Jane Pearson",
    message: "🔥 💭",
    time: "FRIDAY",
    count: 0,
  },
]);
</script>

<template>
  <ChatHeader />

  <template v-for="(chat, key) in chats" :key="key">
    <RouterLink to="/messages">
        <ChatList :chat="chat" />
    </RouterLink>
  </template>
</template>
