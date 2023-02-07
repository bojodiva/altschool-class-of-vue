<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { ref, reactive } from "@vue/reactivity";
import { useMessageColor } from "./composables/useMessageColor.js"

export default {
  setup() {
    const { colors, message, matchColor } = useMessageColor();
    
    return{
    {colors, message, matchColor};
    }
  },
};
</script>

<style></style>
