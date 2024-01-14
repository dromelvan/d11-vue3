<template>
  <v-app>
    <d11-app-bar-navigation-drawer v-if="smAndDown" />
    <d11-app-bar v-else />
  </v-app>
</template>

<script setup>
import D11AppBar from "@/components/app-bar/AppBarMenu.vue";
import D11AppBarNavigationDrawer from "@/components/app-bar/AppBarNavigationDrawer.vue";
import { useDisplay } from "vuetify";

const { smAndDown } = useDisplay();
</script>
