<template>
  <v-container>
    <v-layout>
      <v-col :cols="12">
        <v-timeline>
          <v-timeline-item v-for="item in career_lists" :key="item.year" :right="time_line.right" :small="time_line.small">
            <template v-slot:icon>
              <v-avatar v-if="avatar">
                <img src="http://i.pravatar.cc/64">
              </v-avatar>
            </template>
            <span slot="opposite">{{ item.year }}</span>
            <v-card class="elevation-2">
              <v-card-title class="headline">{{ item.title }}</v-card-title>
              <v-card-text>
                {{ item.description }}
              </v-card-text>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-col>
  </v-layout>
</v-container>
</template>
<script>
  export default {
    name: "Career",
    data: () => ({
      time_line: {
        small: true,
        right: false,
      },
      career_lists: [
        {year: "2017/3", title: "島根職業能力開発短期大学校卒業", description: "電子回路設計のほか組み込みプログラミング、.NET FrameworkでのGUIアプリケーション開発など学んだ。"},
        {year: "2017/4", title: "近畿職業能力開発大学校入学", description: "pythonのTkinterでGUIアプリをつくったりpygameでインベーダーゲームもどきを作って遊ぶ"},
        {year: "2018/8", title: "近畿職業能力開発大学校中途退学", description: "授業内容に興味が湧かなかったため辞める。"},
        {year: "2018/8～2019/7", title: "遊ぶ", description: "バイトや派遣などでのんびりしていた"},
        {year: "2019/8", title: "webサイトを作り始める", description: "ホームページを作る仕事をする。ワードプレスなどをしていた"},
        {year: "2020/7", title: "仕事をやめる", description: "給料が低かったのと、サーバサイドのスキルを身に着けたかったためやめる"},
        {year: "2020/8", title: "仕事を始める", description: "現在に至る"},
      ]
    }),
  }
</script>