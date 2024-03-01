<script setup>
import { computed } from 'vue'
import { usePage } from '@inertiajs/vue3'
import { useMainStore } from '@/Stores/main'
import UserAvatar from '@/Components/UserAvatar.vue'

const mainStore = useMainStore()
const userName = computed(() => usePage().props.auth.user.name)
</script>

<template>
  <UserAvatar :username="userName" :avatar="initials">
    <slot />
  </UserAvatar>
</template>
