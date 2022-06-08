<template>
  <div>
    <label for="genre">Genre:</label>
    <select name="genre" v-model="states.selectedGenre">
      <option value="">Tutti</option>
      <option v-for="(genre, idx) in genres" :key="idx" :value="genre">
        {{ genre }}
      </option>
    </select>
  </div>
</template>

<script>
import states from "@/shared/states";

export default {
  name: "MSelectGenre",
  props: {
    genres: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      states,
    };
  },
};
</script>
