<template>
  <main class="w-full px-5 mx-auto md:w-3/4 md:px-0 py-14">
    <div v-if="albums.length >= 10" class="grid-album">
      <MCardAlbum v-for="(album, idx) in albums" :key="idx" :album="album" />
    </div>
    <div v-else class="flex items-center justify-center">
      <SyncLoader color="#2ABE58" />
    </div>
  </main>
</template>

<script>
import axios from "axios";

import MCardAlbum from "../molecules/MCardAlbum.vue";
import SyncLoader from "../loaders/SyncLoader.vue";
export default {
  components: { MCardAlbum, SyncLoader },
  name: "OMain",
  data() {
    return {
      albums: [],
    };
  },
  created() {
    axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((response) => {
      this.albums = response.data.response;
    });
  },
};
</script>

<style lang="scss" scoped>
.grid-album {
  @apply grid
    justify-center
    sm:grid-cols-2
    md:grid-cols-3
    lg:grid-cols-4
    xl:grid-cols-5
    gap-x-10
    gap-y-6;
}
</style>
