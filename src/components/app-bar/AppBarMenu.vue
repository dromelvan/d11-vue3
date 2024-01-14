<template>
  <v-app-bar color="primary" image="@/assets/images/app-bar-background.png">
    <v-img
      max-height="40"
      max-width="100"
      contain
      src="@/assets/images/d11-logo.png"
    />

    <v-menu class="text-menu" transition="no-transition">
      <template v-slot:activator="{ props }">
        <v-btn v-bind="props" variant="plain" :ripple="false"> Info </v-btn>
      </template>
      <v-list>
        <v-list-item :to="'/rules'" :ripple="false"> Rules </v-list-item>
        <v-list-item :to="'/about'" :ripple="false"> About D11 </v-list-item>
      </v-list>
    </v-menu>
  </v-app-bar>
</template>

<script setup></script>
