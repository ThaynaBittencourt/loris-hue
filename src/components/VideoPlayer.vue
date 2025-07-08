<template>
  <div
    class="relative w-full max-w-4xl mx-auto rounded-xl overflow-hidden shadow-lg"
  >
    <video
      ref="videoRef"
      class="w-full h-auto"
      :src="src"
      :poster="poster"
      @click="togglePlay"
      :controls="showControls"
    ></video>

    <!-- Botão de play central -->
    <button
      v-if="!isPlaying"
      @click="togglePlay"
      class="absolute inset-0 flex items-center justify-center bg-black/40 backdrop-blur-sm transition-all duration-300 hover:bg-black/60"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-20 w-20 text-white opacity-80 hover:opacity-100 transition"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        stroke-width="1.5"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M8 5v14l11-7L8 5z"
        />
      </svg>
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const props = defineProps<{
  src: string;
  poster?: string;
}>();

const videoRef = ref<HTMLVideoElement | null>(null);
const isPlaying = ref(false);
const showControls = ref(false);

const togglePlay = () => {
  if (!videoRef.value) return;

  if (videoRef.value.paused) {
    videoRef.value.play();
    isPlaying.value = true;
    showControls.value = true;
  } else {
    videoRef.value.pause();
    isPlaying.value = false;
  }
};
</script>

<style scoped>
video {
  cursor: pointer;
}
</style>
