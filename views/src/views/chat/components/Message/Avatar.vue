<script lang="ts" setup>
import { computed } from 'vue'
import { NAvatar } from 'naive-ui'
import { useUserStore } from '@/store'
import { isString } from '@/utils/is'
import defaultAvatar from '@/assets/avatar.jpg'

interface Props {
  image?: boolean
}
defineProps<Props>()

const userStore = useUserStore()

const avatar = computed(() => userStore.userInfo.avatar)
</script>

<template>
  <template v-if="image">
    <NAvatar v-if="isString(avatar) && avatar.length > 0" :src="avatar" :fallback-src="defaultAvatar" />
    <NAvatar v-else round :src="defaultAvatar" />
  </template>
  <span v-else class="text-[28px] dark:text-white">
    <svg t="1713670967330" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2930" width="32" height="32" xmlns:xlink="http://www.w3.org/1999/xlink"><path d="M981.333333 618.666667h-106.666666v-21.333334a298.666667 298.666667 0 0 0-118.186667-244.053333l103.893333-162.986667a64 64 0 1 0-36.053333-23.04l-103.04 162.133334A416.213333 416.213333 0 0 0 512 277.333333a416.213333 416.213333 0 0 0-209.28 52.053334l-103.04-162.133334a64 64 0 1 0-36.053333 23.04l103.893333 162.986667A298.666667 298.666667 0 0 0 149.333333 597.333333v21.333334H42.666667v256h106.666666v85.333333h725.333334v-85.333333h106.666666zM85.333333 832v-170.666667h64v170.666667z m746.666667 85.333333H192V597.333333c0-192 160.64-277.333333 320-277.333333s320 85.333333 320 277.333333v320z m106.666667-85.333333h-64v-170.666667h64z" p-id="2931"></path><path d="M405.333333 661.333333m-42.666666 0a42.666667 42.666667 0 1 0 85.333333 0 42.666667 42.666667 0 1 0-85.333333 0Z" p-id="2932"></path><path d="M618.666667 661.333333m-42.666667 0a42.666667 42.666667 0 1 0 85.333333 0 42.666667 42.666667 0 1 0-85.333333 0Z" p-id="2933"></path><path d="M661.333333 533.333333H362.666667a128 128 0 0 0 0 256h298.666666a128 128 0 0 0 0-256z m0 213.333334H362.666667a85.333333 85.333333 0 0 1 0-170.666667h298.666666a85.333333 85.333333 0 0 1 0 170.666667z" p-id="2934"></path>
    </svg>
  </span>
</template>
