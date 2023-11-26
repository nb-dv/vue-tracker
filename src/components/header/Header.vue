<script setup>
import { CheckIcon } from '@heroicons/vue/24/solid'
</script>

<template>
  <header class="sticky top-0 z-20 flex items-center justify-between border-b bg-white p-3">
    <a>Logo</a>
    <a href="#" class="text-sm">
      <div v-if="true" class="flex items-center gap-1">
        Day complete!
        <CheckIcon class="h-7 text-green-500"/>
      </div>
      <div v-else class="flex items-center gap-1">
        Progress:
        <span class="font-mono">20%</span>
        <span class="h-3 w-3 rounded full bg-red-500"></span>
      </div>
    </a>
  </header>
</template>