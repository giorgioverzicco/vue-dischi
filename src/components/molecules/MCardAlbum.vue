<template>
  <div class="flex flex-col items-center justify-center gap-5 p-5 bg-slate-blue-500">
    <AThumbnail :thumbnail="{ src: 'https://via.placeholder.com/300', alt: 'Blank' }" />
    <ATitle class="text-center uppercase" content="Album Title" />
    <div class="leading-5 text-center text-gray-500">
      <p class="text-lg font-medium">Album Artist</p>
      <p>0000</p>
    </div>
  </div>
</template>

<script>
import AThumbnail from "../atoms/AThumbnail.vue";
import ATitle from "../atoms/ATitle.vue";
export default {
  components: { AThumbnail, ATitle },
  name: "MCardAlbum",
};
</script>
