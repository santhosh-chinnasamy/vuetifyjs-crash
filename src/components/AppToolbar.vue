<template>
  <v-toolbar color="indigo" dark>
    <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
  <router-link to="/">
  <v-toolbar-title class="white--text">Santhosh</v-toolbar-title>
  </router-link>
    <v-spacer></v-spacer>
      <v-badge left bottom color="red">
      <span slot="badge">6</span>
      <v-icon
        large
        color="red lighten-1"
      >
        shopping_cart
      </v-icon>
    </v-badge>

    <div>
      <v-toolbar-items class="hidden-sm-and-down">
      <v-btn flat>About</v-btn>
      <router-link to="/contact"><v-btn flat>Contact</v-btn></router-link>
      <router-link to="/login"><v-btn flat>Login</v-btn></router-link>
    </v-toolbar-items>
    </div>

    <div class="hidden-md-and-up">
     <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      height="400px"
    >
      <v-list class="pa-1">
        <v-list-tile avatar>
          <v-list-tile-avatar>
            <img src="https://randomuser.me/api/portraits/men/85.jpg">
          </v-list-tile-avatar>

          <v-list-tile-content>
            <v-list-tile-title>John Leider</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>

      <v-list class="pt-0" dense>
        <v-divider></v-divider>

        <v-list-tile
          v-for="item in items"
          :key="item.title"
        >
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>

          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>

    
    </div>
    
  </v-toolbar>
</template>

<script>
export default {
  data() {
    return {
      drawer: null,
      items: [
        { title: "Home", icon: "dashboard" },
        { title: "About", icon: "question_answer" }
      ],
      mini: false,
      right: null
    };
  }
};
</script>
