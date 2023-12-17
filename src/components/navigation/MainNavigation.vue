<script setup>
import { ClockIcon, ListBulletIcon, ChartBarIcon } from '@heroicons/vue/24/outline'
import NavigationItem from './NavigationItem.vue'

const navList = {
  timeline: ClockIcon,
  activities: ListBulletIcon,
  progress: ChartBarIcon,
}

const currentPage = 'timeline'
</script>

<template>
  <nav class="sticky bottom-0 z-10 bg-white">
    <ul class="flex items-center justify-around border-t">
      <NavigationItem
        v-for="(icon, page) in navList"
        :key="page"
        :href="`#${page}`"
        :class="{ 'bg-grey-200': currentPage === 'timeline' }"
      >
        <component :is="icon" class="h-6"/>
        {{ page }}
      </NavigationItem>
    </ul>
  </nav>
</template>