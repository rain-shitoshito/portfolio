<template>
  <v-footer app dark padless>
    <v-card flat tile class="lighten-1 white--text text-center w-100">
      <v-card-text>
        <v-btn v-for="item in link_lists" :key="item.icon" :href="item.link" class="mx-4 white--text" icon>
          <v-icon size="24px">
            {{ item.icon }}
          </v-icon>
        </v-btn>
      </v-card-text>
      <v-divider></v-divider>
      <v-card-text class="white--text">
        {{ year }} Takuma Maeda
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      link_lists: [
        {icon: "mdi-github", link: "https://github.com/rain-shitoshito"}
      ],
    }
  },
  computed: {
      year: function() {
          return new Date().getFullYear()
      }
  }
};
</script>