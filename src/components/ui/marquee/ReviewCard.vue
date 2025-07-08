<template>
  <figure
    class="relative w-64 cursor-pointer overflow-hidden rounded-xl border border-white/10 bg-[#201e34] p-4 shadow-lg transition-all duration-300 hover:-translate-y-1 hover:shadow-xl dark:border-white/20 dark:bg-[#18171f]"
  >
    <div class="flex flex-row items-center gap-2">
      <img :src="img" class="rounded-full" width="32" height="32" alt="" />
      <div class="flex flex-col">
        <span class="text-sm font-medium dark:text-white">
          {{ name }}
        </span>
        <p class="text-xs font-medium text-white/40">{{ username }}</p>
      </div>
    </div>
    <blockquote class="mt-2 text-sm text-white">{{ body }}</blockquote>
  </figure>
</template>

<script lang="ts" setup>
interface Props {
  img: string;
  name: string;
  username: string;
  body: string;
}

defineProps<Props>();
</script>
