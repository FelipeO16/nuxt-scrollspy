# Setup

Look at the [Nuxt 3 documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.


## Dependencies

• [VueUse](https://vueuse.org/)

• [Tailwindcss](https://tailwindcss.com/)

## How to use

```html
<!-- main -->
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
      Lorem...
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
      Lorem...
    </div>
  </Scroll>

  <!-- menu -->
  <div class="<classes>">
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
```

```html
<script setup lang="ts">
let active = ref("");
const setActive = (name: string) => {
  active.value = name;
};
</script>
```

### Preview
![](https://cdn.discordapp.com/attachments/884496726105403464/1215021765181444226/localhost_3000_home-6March2024-ezgif.com-video-to-gif-converter_1.gif?ex=65fb3c32&is=65e8c732&hm=73742156ea479bf193b9a2a42e29eb4404476ade8930270b250fb0ccacabd8f4&)