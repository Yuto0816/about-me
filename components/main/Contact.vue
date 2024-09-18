<template>
  <v-card id="contact" class="my-4">
    <v-card-title class="text-h4">Contact</v-card-title>
    <v-card-text>
      <v-form @submit.prevent="submitForm">
        <v-text-field
          v-model="name"
          label="名前"
          required
          outlined
        ></v-text-field>
        <v-text-field
          v-model="email"
          label="メール"
          type="email"
          required
          outlined
        ></v-text-field>
        <v-textarea
          v-model="message"
          label="メッセージ"
          required
          outlined
        ></v-textarea>
        <v-btn type="submit" color="primary" block :loading="loading">
          送信
        </v-btn>
      </v-form>
    </v-card-text>
  </v-card>
</template>

<script lang="ts">
export default defineNuxtComponent({
  name: "Contact",
  data() {
    return {
      name: "",
      email: "",
      message: "",
      loading: false,
    };
  },
  methods: {
    submitForm() {
      this.loading = true;
      // フォーム送信のロジックをここに追加
      setTimeout(() => {
        alert(
          `名前: ${this.name}\nメール: ${this.email}\nメッセージ: ${this.message}`
        );
        this.loading = false;
        this.name = "";
        this.email = "";
        this.message = "";
      }, 1000);
    },
  },
});
</script>

<style scoped>
#contact {
  padding: 2rem;
  background-color: #fafafa;
}
form div {
  margin-bottom: 1rem;
}
label {
  display: block;
  margin-bottom: 0.5rem;
}
input,
textarea {
  width: 100%;
  padding: 0.5rem;
  box-sizing: border-box;
}
button {
  padding: 0.5rem 1rem;
}
</style>
