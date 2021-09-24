<template>

<v-app>
  <v-navigation-drawer app>
    <!-- -->
    <router-link to="/">Home</router-link>
    <router-link to="/about">About</router-link>
    <router-link to="/ongoing">Ongoing</router-link>
    <router-link to="/completed">Completed</router-link>
  </v-navigation-drawer>

  <v-app-bar app>
    <!-- -->
  </v-app-bar>

  <!-- Sizes your content based upon application components -->
  <v-main>

    <!-- Provides the application the proper gutter -->
    <v-container fluid>

      <!-- If using vue-router -->
      <router-view></router-view>
    </v-container>
  </v-main>

  <v-footer app>
    <p style="color:tomato">footer</p>
  </v-footer>
</v-app>

    
</template>

<script>


export default {
  name: "App",
  components: {
    //
  },
  data() {
    return {
      //
    };
  }
};
</script>
