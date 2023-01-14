<template>
  <v-app dark>
    <v-navigation-drawer app>
      <SideBar />
    </v-navigation-drawer>
    
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <!-- <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer> -->
  </v-app>
</template>

<script>
import SideBar from '../components/common/SideBar.vue';

export default {
    name: "DefaultLayout",
    data() {
        return {};
    },
    components: { SideBar }
}
</script>
