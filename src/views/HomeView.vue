<script setup lang="ts">
import { ref } from 'vue';

const referencia = ref<string[]>(['s', 'e', 'x', 'o']); // Declare a ref como um array de strings

function delay(ms: number) {
  return new Promise((resolve) => setTimeout(resolve, ms));
}


</script>

<template>
  <v-container class="h-screen bg-primary pa-0" fluid>
    <v-row>
      <v-col cols="12" lg="6" class="d-flex flex-column justify-center align-center">
        <h1 class="text-h2">Matheus Luna</h1>
        <span class="text-h2 mt-5 d-flex" v-for="letra in referencia">{{ letra }}</span>
        <aside>
          <p class="text-h5 mt-5">Sou um Dev. iniciante apaixonado por aprender e Desenvolver</p>
        </aside>
        <section class="d-flex w-50 justify-center mt-5" style="gap: 20px">
          <v-btn variant="outlined">Linked-in</v-btn>
          <v-btn variant="outlined">Curriculum</v-btn>
        </section>
      </v-col>
      <v-col cols="12" lg="6" class="d-flex justify-center align-center justify-center">
        <v-img src="./src/assets/gatchonix.jpg" class="rounded-pill mx-2 border-md border-secondary border-opacity-100" draggable="false"></v-img>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" lg="12" class="d-flex flex-column align-center">
        <h1 class="text-h1">Tecnoogias</h1>
        <span class="text-h5 mt-4">Atualmente essas são as tecnologias que mais vejo no meu dia a dia.</span>
        <v-list class="d-flex justify-center bg-primary flex-wrap">
          <v-list-item>
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg" draggable="false" class="tecnologies-icons"/>
          </v-list-item>
          <v-list-item>
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original.svg" draggable="false" class="tecnologies-icons"/>
          </v-list-item>
          <v-list-item>
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg"draggable="false" class="tecnologies-icons"/>
          </v-list-item>
          <v-list-item>
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/bootstrap/bootstrap-original.svg" draggable="false" class="tecnologies-icons"/>
          </v-list-item>
          <v-list-item>
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/laravel/laravel-original.svg" draggable="false"class="tecnologies-icons"/>
          </v-list-item>
          <v-list-item>
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vuejs/vuejs-original.svg" draggable="false"class="tecnologies-icons"/>
          </v-list-item>

          <v-list-item>
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vuetify/vuetify-original.svg" draggable="false" class="tecnologies-icons"/>
          </v-list-item>
          <v-list-item >
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/tailwindcss/tailwindcss-original.svg" draggable="false" class="tecnologies-icons"/>
          </v-list-item>
        </v-list>
      </v-col>
    </v-row>
  </v-container>
</template>draggble

<style scoped>
  .tecnologies-icons{
    width: 150px;
    height: 150px;
    width: 70%;
    filter: grayscale(100%);
    cursor: pointer;
  }

.tecnologies-icons:hover {
    animation: dropzin 0.3s forwards ease-out;
}

@keyframes dropzin {
    0% {
        filter: drop-shadow(0px 0px 0px #000);
    }

    100% {
        filter: drop-shadow(0px 0px 4px rgba(53, 235, 86, 0.744));
    }
}

</style>
