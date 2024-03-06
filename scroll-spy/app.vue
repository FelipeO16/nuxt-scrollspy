<template>
  <div class="w-screen h-screen bg-gray-800 flex">
    <div class="bar w-full h-full overflow-auto">
      <div class="w-5/6 h-full space-y-8 p-8">
        <Scroll
          title="Seja Bem-Vindo"
          id="home"
          @isActive="setActive('home')"
          :pt="{
            title: 'text-4xl px-4',
          }"
        >
          <div class="text-white py-4">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit sequi
            eaque doloremque placeat laborum odit, hic ratione dolore rerum
            officiis sint cumque, quis est at a adipisci beatae iusto facilis.
          </div>
        </Scroll>

        <Scroll
          title="Área de contatos"
          id="contact"
          @isActive="setActive('contact')"
          :pt="{
            title: 'text-4xl px-4',
          }"
        >
          <div class="text-white py-4">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit sequi
            eaque doloremque placeat laborum odit, hic ratione dolore rerum
            officiis sint cumque, quis est at a adipisci beatae iusto facilis.
          </div>
        </Scroll>
      </div>
      <div
        class="absolute right-0 top-0 w-1/6 h-full bg-gray-950 p-8 flex flex-col text-lg text-gray-500 items-start gap-2"
      >
        <button
          :class="{ 'border-l-2 text-gray-100': active == 'home' }"
          class="px-3 border-gray-500 transition-all duration-150 ease-linear"
        >
          <a href="#home">Home</a>
        </button>
        <button
          :class="{ 'border-l-2 text-gray-100': active == 'contact' }"
          class="px-3 border-gray-500 transition-all duration-150 ease-linear"
        >
          <a href="#contact">Contato</a>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
let active = ref("");
const setActive = (name: string) => {
  active.value = name;
};
</script>

<style scoped>
* {
  scroll-behavior: smooth;
}
</style>
