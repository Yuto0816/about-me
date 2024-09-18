<template>
  <v-card id="skills" class="my-4">
    <v-card-title class="text-h4">Skills</v-card-title>
    <v-card-text>
      <v-list>
        <v-list-item v-for="(skill, index) in skills" :key="index">
          <template v-slot:prepend>
            <v-icon color="primary">mdi-check-circle</v-icon>
          </template>
          {{ skill }}
        </v-list-item>
      </v-list>
    </v-card-text>
  </v-card>
</template>

<script lang="ts">
export default defineNuxtComponent({
  name: "Skills",
  data() {
    return {
      skills: [
        "JavaScript / TypeScript",
        "Vue.js / Nuxt.js",
        "HTML & CSS",
        "Git & GitHub",
      ],
    };
  },
});
</script>

<style scoped>
#skills {
  padding: 2rem;
}
ul {
  list-style: square;
}
</style>
