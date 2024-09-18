<template>
  <v-card id="profile" class="my-4">
    <v-card-title class="text-h4">Profile</v-card-title>
    <v-card-text>
      <v-container>
        <AboutmeName />
      </v-container>
    </v-card-text>
  </v-card>
</template>

<script lang="ts">
export default defineNuxtComponent({
  name: "Profile",
});
</script>

<style scoped>
#profile {
  padding: 2rem;
  background-color: #fafafa;
}
</style>
