<template>
  <div class="bg-[#d5417d] h-[10px]"></div>
  <div class="bg-[#201e34]">
    <div class="flex flex-col items-center justify-center relative mt-20">
      <div class="mb-10 flex flex-col items-center">
        <img src="/img/lorishue.png" alt="" class="w-50 z-10" />

        <!-- Imagem de fundo/base (centro) -->
        <img src="/img/textIndex.png" alt="" class="w-[800px]" />

        <!-- Vídeo na parte de baixo -->
        <div class="w-full flex justify-center mt-40">
          <VideoPlayer
            src="../img/larishueVideo.mp4"
            poster="/img/thumb.png"
            class="max-w-[800px] max-h-[500px]"
          />
        </div>
      </div>

      <div style="margin-top: 5.5rem">
        <Button class="neon-button w-full max-w-[300px] cursor-pointer">
          QUERO APRENDER RESINA
        </Button>
      </div>
    </div>

    <!-- SVGs -->
    <div class="inset-0 pointer-events-none z-20">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1000 100"
        preserveAspectRatio="none"
        style="
          transform: rotate(180deg);
          width: 100%;
          height: 20%;
          margin-top: 450px;
          margin-bottom: -0.5px;
        "
      >
        <path
          class="elementor-shape-fill"
          style="fill: #d5417d"
          d="M421.9,6.5c22.6-2.5,51.5,0.4,75.5,5.3c23.6,4.9,70.9,23.5,100.5,35.7c75.8,32.2,133.7,44.5,192.6,49.7
          c23.6,2.1,48.7,3.5,103.4-2.5c54.7-6,106.2-25.6,106.2-25.6V0H0v30.3c0,0,72,32.6,158.4,30.5c39.2-0.7,92.8-6.7,134-22.4
          c21.2-8.1,52.2-18.2,79.7-24.2C399.3,7.9,411.6,7.5,421.9,6.5z"
        />
      </svg>
    </div>
    <div
      class="relative flex h-screen w-full items-center justify-center overflow-hidden"
    >
      <!-- Imagem de fundo -->

      <!-- Cor sobreposta com opacidade -->
      <div class="absolute inset-0 bg-[#d5417d]/80">
        <img
          src=""
          alt="Background"
          class="absolute inset-0 h-[1200px] w-full object-cover opacity-5"
        />
      </div>

      <!-- Conteúdo -->
      <div class="relative z-10 text-center">
        <h1
          class="font-sans text-2xl font-bold text-white lg:text-3xl md:text-5xl"
        >
          <strong>A iniciativa de iniciar começa por</strong>
          <br />
          <strong>de iniciar começa por diversos motivos, seja ele:</strong>
        </h1>
      </div>
    </div>
  </div>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 1000 100"
    preserveAspectRatio="none"
  >
    <path
      class="elementor-shape-fill1"
      style="fill: #b13a6e"
      d="M421.9,6.5c22.6-2.5,51.5,0.4,75.5,5.3c23.6,4.9,70.9,23.5,100.5,35.7c75.8,32.2,133.7,44.5,192.6,49.7
      c23.6,2.1,48.7,3.5,103.4-2.5c54.7-6,106.2-25.6,106.2-25.6V0H0v30.3c0,0,72,32.6,158.4,30.5c39.2-0.7,92.8-6.7,134-22.4
      c21.2-8.1,52.2-18.2,79.7-24.2C399.3,7.9,411.6,7.5,421.9,6.5z"
    ></path>
  </svg>
  <!-- MAIS IDEISAS A BAIXO -->
  <div class="flex justify-center items-center min-h-screen bg-white gap-x-6">
    <CardHover
      src="/public/img/resina 1.jpg"
      alt="Artista com obra em resina"
    />
    <CardHover
      src="/public/img/resina 2.jpg"
      alt="Artista com obra em resina"
    />
    <CardHover
      src="/public/img/resina 3.jpg"
      alt="Artista com obra em resina"
    />
    <CardHover
      src="/public/img/resina 4.jpg"
      alt="Artista com obra em resina"
    />
  </div>
  <!-- comentarios -->

  <div
    class="relative bg-[#201e34] flex h-[500px] w-full flex-col items-center justify-center overflow-hidden"
  >
    <!-- First Marquee -->
    <Marquee pause-on-hover class="[--duration:20s]">
      <ReviewCard
        v-for="review in firstRow"
        :key="review.username"
        :img="review.img"
        :name="review.name"
        :username="review.username"
        :body="review.body"
      />
    </Marquee>

    <!-- Second Marquee (reverse) -->
    <Marquee reverse pause-on-hover class="[--duration:20s]">
      <ReviewCard
        v-for="review in secondRow"
        :key="review.username"
        :img="review.img"
        :name="review.name"
        :username="review.username"
        :body="review.body"
      />
    </Marquee>

    <!-- Left Gradient -->
  </div>
  <div
    style="
      margin-top: -1px;
      /* margin-bottom: 100px; */
      width: 100%;
      position: absolute;
    "
  >
    <svg
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 1000 100"
      preserveAspectRatio="none"
    >
      <path
        class="elementor-shape-fill1"
        style="fill: #201e34"
        d="M421.9,6.5c22.6-2.5,51.5,0.4,75.5,5.3c23.6,4.9,70.9,23.5,100.5,35.7c75.8,32.2,133.7,44.5,192.6,49.7
      c23.6,2.1,48.7,3.5,103.4-2.5c54.7-6,106.2-25.6,106.2-25.6V0H0v30.3c0,0,72,32.6,158.4,30.5c39.2-0.7,92.8-6.7,134-22.4
      c21.2-8.1,52.2-18.2,79.7-24.2C399.3,7.9,411.6,7.5,421.9,6.5z"
      ></path>
    </svg>
  </div>
  <div class="flex justify-center items-center min-h-screen bg-white px-6">
    <!-- Imagem -->
    <div>
      <img
        src="../img/michele1.jpg"
        alt="Maria Michele"
        class="w-[500px] rounded-2xl shadow-lg"
      />
    </div>

    <!-- Texto -->
    <div
      class="ml-12 bg-white shadow-xl rounded-2xl p-8 max-w-lg"
      style="margin-left: -50px"
    >
      <h2 class="text-2xl font-bold text-[#1c114c]">Maria Michele</h2>
      <p class="text-lg font-medium text-gray-600 mb-5">26 anos</p>
      <div class="w-16 h-1 bg-[#d5417d] mb-4 rounded"></div>

      <p class="text-gray-700 leading-relaxed">
        Graduada em Administração com MBA em finanças e após descobrir meu
        propósito de vida fiz a transição do mundo corporativo para empreender
        no Universo da Resina.
      </p>
      <p class="mt-4 text-gray-700 leading-relaxed">
        Após várias dificuldades enfrentadas no início, pela ausência de
        referências e materiais técnicos no mercado brasileiro, fundei a Escola
        da Resina, que através de técnicas traduzidas e autorais, criei minha
        própria metodologia de trabalho e vim a ser sucesso no Brasil.
      </p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Marquee from "@/components/ui/marquee/Marquee.vue";
import ReviewCard from "@/components/ui/marquee/ReviewCard.vue";
import CardHover from "@/components/CardHover.vue";
import VideoPlayer from "@/components/VideoPlayer.vue";
import ColourfulText from "@/components/ui/colourful-text/ColourfulText.vue";
import Button from "@/components/ui/button/Button.vue";

// Reviews data
const reviews = [
  {
    name: "Lucas",
    username: "@lucas",
    body: "O trabalho com resina está simplesmente impecável, cada detalhe demonstra muita habilidade e paixão!",
    img: "https://avatar.vercel.sh/lucas",
  },
  {
    name: "Mariana",
    username: "@mariana",
    body: "Fiquei encantada com a delicadeza das peças. É arte que transforma e emociona!",
    img: "https://avatar.vercel.sh/mariana",
  },
  {
    name: "Carlos",
    username: "@carlos",
    body: "A criatividade e o acabamento das peças de resina são de outro nível. Parabéns pelo talento!",
    img: "https://avatar.vercel.sh/carlos",
  },
  {
    name: "Fernanda",
    username: "@fernanda",
    body: "Cada peça é uma verdadeira obra de arte. Admiro muito o cuidado e a técnica envolvidos!",
    img: "https://avatar.vercel.sh/fernanda",
  },
  {
    name: "Pedro",
    username: "@pedro",
    body: "Surpreendente como a resina ganha vida nas mãos do artista. Trabalho excepcional!",
    img: "https://avatar.vercel.sh/pedro",
  },
  {
    name: "Aline",
    username: "@aline",
    body: "O acabamento perfeito e a originalidade das peças mostram um talento raro. Parabéns!",
    img: "https://avatar.vercel.sh/aline",
  },
];

// Split reviews into two rows
const firstRow = ref(reviews.slice(0, reviews.length / 2));
const secondRow = ref(reviews.slice(reviews.length / 2));

const images = [
  "https://images.unsplash.com/photo-1541701494587-cb58502866ab?q=80&w=3870&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
  "https://images.unsplash.com/photo-1541701494587-cb58502866ab?q=80&w=3870&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
  "https://images.unsplash.com/photo-1541701494587-cb58502866ab?q=80&w=3870&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
  "https://images.unsplash.com/photo-1541701494587-cb58502866ab?q=80&w=3870&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
];
</script>

<style>
.elementor-shape-fill {
  fill: #d5417d;
  opacity: 80%;
}
.elementor-shape-fill1 {
  fill: #d5417d;
  opacity: 100%;
}
.elementor-shape-fill2 {
  fill: #d5417d;
  opacity: 100%;
}
.teste {
  rotate: 100deg;
}
</style>
