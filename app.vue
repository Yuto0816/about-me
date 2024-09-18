<template>
  <v-app>
    <v-app-bar app color="black" dark>
      <v-toolbar-title>自己紹介サイト</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text href="#about">About</v-btn>
      <v-btn text href="#skills">Skills</v-btn>
      <v-btn text href="#contact">Contact</v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <MainProfile />
        <MainSkills />
        <MainContact />
      </v-container>
    </v-main>

    <v-footer app color="black" dark>
      <v-col class="text-center" cols="12">
        © {{ new Date().getFullYear() }} 自己紹介サイト
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",
};
</script>
