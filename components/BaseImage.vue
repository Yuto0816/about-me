<template>
  <img :src="fullPath" :alt="alt" />
</template>

<script lang="ts">
export default defineNuxtComponent({
  props: {
    src: {
      type: String,
      required: true,
    },
    alt: {
      type: String,
      default: "",
    },
  },
  computed: {
    baseURL() {
      const config = useRuntimeConfig();
      return config.app.baseURL.replace(/\/$/, "");
    },
    fullPath() {
      return this.baseURL + "/" + this.src.replace(/^\//, "");
    },
  },
});
</script>
