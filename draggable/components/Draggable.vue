<template>
  <div class="fixed" ref="el" :style="style">
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import { useDraggable } from "@vueuse/core";
const el = ref<HTMLElement | null>(null);

const props = defineProps<{
  px: number;
  py: number;
}>();

const { x, y, style } = useDraggable(el, {
  initialValue: { x: props.px, y: props.py },
});
</script>
