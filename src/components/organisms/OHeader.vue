<template>
  <header class="flex items-center h-20 px-5 py-3 bg-slate-blue-500">
    <ALogo />
  </header>
</template>

<script>
import ALogo from "../atoms/ALogo.vue";
export default {
  name: "OHeader",
  components: { ALogo },
};
</script>
