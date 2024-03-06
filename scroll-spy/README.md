# Setup

Look at the [Nuxt 3 documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.


## Dependencies

• [VueUse](https://vueuse.org/)

• [Tailwindcss]([https://tailwindcss.)

## How to use

```html
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
</div>
```

```ts
<script setup lang="ts">
let active = ref("");
const setActive = (name: string) => {
  active.value = name;
};
</script>
```

### Preview
![](https://cdn.discordapp.com/attachments/884496726105403464/1215008804840931369/localhost_3000_home-6March2024-ezgif.com-video-to-gif-converter.gif?ex=65fb3020&is=65e8bb20&hm=4b2f0dd7159e5373d97f93dd2d79e1631fda92e98cf0b092286bdf165a6a5735&)