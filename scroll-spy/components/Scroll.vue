<script setup lang="ts">
import { useIntersectionObserver } from "@vueuse/core";

const props = defineProps<{
  title: string;
  pt?: {
    root?: string;
    title?: string;
    content?: string;
  };
}>();

const target = ref(null);
const targetIsVisible = ref(false);

const { stop } = useIntersectionObserver(
  target,
  ([{ isIntersecting }], observerElement) => {
    targetIsVisible.value = isIntersecting;
  }
);

const emit = defineEmits(["isActive"]);

watch(targetIsVisible, () => {
  if (targetIsVisible.value) {
    emit("isActive");
  }
});
</script>

<template>
  <div :class="pt?.root" class="root w-full h-full">
    <div ref="target" class="target">
      <h1 :class="pt?.title" class="text-white">
        <span class="text-cyan-500">#</span>{{ title }}
      </h1>
    </div>
    <div :class="pt?.content">
      <slot></slot>
    </div>
  </div>
</template>
