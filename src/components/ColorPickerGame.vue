<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { color } from "../composables/color";
export default {
  setup() {
    const game = color();
    return {
      colors: game.colors,
      message: game.message,
      matchColor: game.matchColor,
    };
  },
};
</script>

<style></style>
