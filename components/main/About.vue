<template>
  <v-card id="about" class="my-4">
    <v-card-title class="text-h4">About Me</v-card-title>
    <v-card-text>
      <v-list>
        <v-list-item
          v-for="(item, index) in aboutItems"
          :key="index"
          class="d-block"
        >
          <v-list-item-title class="text-h6 blue-title mb-2">{{
            item.title
          }}</v-list-item-title>
          <v-list-item-subtitle>
            <div v-if="typeof item.content === 'string'" class="content-text">
              {{ item.content }}
            </div>
            <ul v-else class="content-text">
              <li v-for="(point, pointIndex) in item.content" :key="pointIndex">
                {{ point }}
              </li>
            </ul>
          </v-list-item-subtitle>
        </v-list-item>
      </v-list>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      aboutItems: [
        {
          title: "名前と職業",
          content: "山田太郎 - ソフトウェアエンジニア",
        },
        {
          title: "経歴と学歴",
          content: "東京大学工学部卒業。2015年からIT業界でキャリアをスタート。",
        },
        {
          title: "専門分野とスキル",
          content: [
            "フロントエンド開発 (Vue.js, React)",
            "バックエンド開発 (Node.js, Python)",
            "データベース設計と管理",
            "クラウドインフラストラクチャ (AWS, GCP)",
          ],
        },
        {
          title: "趣味と興味",
          content: ["テニス", "写真撮影", "旅行", "新しい技術の学習"],
        },
        {
          title: "目標と抱負",
          content:
            "AIと機械学習を活用した革新的なアプリケーションの開発に携わり、社会に貢献したいと考えています。",
        },
        {
          title: "パーソナリティと価値観",
          content:
            "チームワークを重視し、常に新しいことに挑戦する姿勢を大切にしています。誠実さと創造性を兼ね備えたエンジニアを目指しています。",
        },
        {
          title: "ユニークな経験や達成",
          content:
            "2019年、国際的なハッカソンで優勝。100か国以上から1000チーム以上が参加する中、革新的なヘルスケアアプリのプロトタイプを開発しました。",
        },
      ],
    };
  },
};
</script>

<style scoped>
#about {
  padding: 2rem;
  background-color: #fafafa;
}

.v-list-item {
  padding-bottom: 1.5rem !important;
}

.blue-title {
  color: #1976d2 !important;
}

.content-text {
  font-size: 1.1rem !important;
  line-height: 1.5 !important;
  white-space: normal !important;
}

ul.content-text {
  padding-left: 1rem;
  margin-top: 0;
}

ul.content-text li {
  margin-bottom: 0.5rem;
}
</style>
