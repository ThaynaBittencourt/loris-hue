<template>
  <div
    class="relative w-64 h-80 overflow-hidden rounded-[30px] shadow-md transition-all duration-300 ease-in-out hover:-translate-y-3 hover:shadow-lg"
    style="border-top-left-radius: 0"
  >
    <img :src="src" :alt="alt" class="object-cover w-full h-full" />
  </div>
</template>

<script setup>
defineProps({
  src: { type: String, required: true },
  alt: { type: String, default: "Imagem do card" },
});
</script>
