<template>
  <v-container class="self-introduction">
    <v-row>
      <v-col cols="12">
        <h2 class="text-h6 blue-title mb-4">自己紹介</h2>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" class="d-flex justify-center">
        <div class="profile-image-container">
          <BaseImage
            src="/img/profile.jpeg"
            alt="プロフィール画像"
            class="profile-image"
          />
        </div>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <div class="content-text mb-2"><strong>名前：</strong>渡邉勇斗</div>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <div class="content-text mb-2"><strong>職業：</strong>ITエンジニア</div>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <div class="content-text mb-2"><strong>年齢：</strong>24歳</div>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <div class="content-text">
          <strong>趣味：</strong>プログラミング、ランニング
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import BaseImage from "~/components/BaseImage.vue";
</script>

<style scoped>
.self-introduction {
  background-color: #f5f5f5;
  border-radius: 8px;
  padding: 16px;
}

.blue-title {
  color: #1976d2;
}

.content-text {
  font-size: 1.1rem;
  line-height: 1.5;
}

.profile-image-container {
  width: 200px; /* 画像の幅を指定 */
  margin-bottom: 16px; /* 画像の下に余白を追加 */
}

.profile-image {
  width: 100%;
  height: auto; /* アスペクト比を保持 */
  object-fit: contain; /* 画像全体を表示 */
}
</style>
