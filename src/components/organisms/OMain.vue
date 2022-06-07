<template>
  <main class="w-full mx-auto md:w-3/4 py-14">
    <div class="grid-album">
      <MCardAlbum />
      <MCardAlbum />
      <MCardAlbum />
      <MCardAlbum />
      <MCardAlbum />
      <MCardAlbum />
    </div>
  </main>
</template>

<script>
import MCardAlbum from "../molecules/MCardAlbum.vue";
export default {
  components: { MCardAlbum },
  name: "OMain",
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
