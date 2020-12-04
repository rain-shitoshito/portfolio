 <template>
  <!-- App.vue -->
  <v-app>
    <v-navigation-drawer app light v-model="drawer" clipped>
      <v-container>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="title grey--text">
              Menu
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>
        <v-list dense nav>
          <v-list-item v-for="nav_list in nav_lists" :key="nav_list.name" :to="nav_list.link">
            <v-list-item-icon>
              <v-icon>{{ nav_list.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>{{ nav_list.name }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-container>
    </v-navigation-drawer>
 
    <v-app-bar app clipped-left>
      <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
      <v-toobar-title>My Portfolio</v-toobar-title>
    </v-app-bar>
 
    <!-- Sizes your content based upon application components -->
    <v-main>
      <!-- Provides the application the proper gutter -->
      <v-container fluid class="h-100">
        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>
    <app-footer></app-footer>
  </v-app>
</template>
 
<script>
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    'app-footer': Footer,
  },
  data() {
    return {
      drawer: null,
      nav_lists:[
        {name: 'Home', icon: 'mdi-home', link: '/'},
        {name: 'Career', icon: 'mdi-human-handsup', link: '/career'},
        {name: 'Skill', icon: 'mdi-hammer-wrench', link: '/skill'},
        {name: 'Contact', icon: 'mdi-email-send-outline', link: '/contact'},
      ]
    }
  }
};
</script>
 
<style>
.w-100 {
  width: 100%;
}
.h-100 {
  height: 100%;
}
.relative {
  position: relative;
}
</style>