<script setup>
import { computed } from 'vue'
import { usePage } from '@inertiajs/vue3'
import UserAvatar from '@/components/UserAvatar.vue'

const userName = computed(() => usePage().props.auth.user.last_name)
</script>

<template>
  <UserAvatar :username="userName" api="initials">
    <slot />
  </UserAvatar>
</template>
