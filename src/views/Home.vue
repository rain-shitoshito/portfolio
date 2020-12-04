<template>
  <v-container>
    <v-row>
      <v-col :cols="12">
        <v-card width="500" elevation="2" class="mx-auto" outlined shaped>
        <v-img
          height="200px"
          src="@/assets/bg.jpg">
          <v-card-title class="white--text mt-8">
            <v-avatar size="80">
              <img
                alt="takuma maeda"
                src="@/assets/icon.png"
              >
            </v-avatar>
            <p class="ml-3 mb-0">Takuma Maeda</p>
          </v-card-title>
        </v-img>
        <v-card-text>
          <div class="font-weight-bold ml-8 mb-2">
            <v-list three-line>
              <v-subheader><h2>About me...</h2></v-subheader>
              <v-list-item v-for="item in info_lists" :key="item.name">
                <v-list-item-avatar>
                  <v-icon :color="item.color">mdi-chevron-right</v-icon>
                </v-list-item-avatar>
                <v-list-item-content>
                  <v-list-item-title>{{ item.title }}</v-list-item-title>
                  <v-list-item-subtitle v-if="item.flag">
                    <v-btn :href="item.link">{{ item.description }}</v-btn>
                  </v-list-item-subtitle>
                  <v-list-item-subtitle v-else>
                    {{ item.description }}
                  </v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </div>
        </v-card-text>
      </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      info_lists:[
        {color: "blue", title: "age", description: "1996/11/07 24歳"},
        {color: "green", title: "product", description: "Github", flag: true, link:"https://github.com/rain-shitoshito"},
        {color: "blue", title: "favorite food", description: "サーモン, 豚骨ラーメン"},
      ]
    }
  }
};
</script>