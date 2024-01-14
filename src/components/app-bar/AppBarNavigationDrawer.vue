<template>
  <v-app-bar
    color="primary"
    :density="density"
    image="@/assets/images/app-bar-background.png"
  >
    <v-app-bar-nav-icon @click="toggleDrawer" />

    <v-spacer v-if="xs" />
    <v-img
      class="d11-logo"
      max-height="38"
      max-width="100"
      contain
      src="@/assets/images/d11-logo.png"
    />
    <v-spacer v-if="xs" />
  </v-app-bar>

  <v-navigation-drawer v-model="drawer">
    <v-list density="compact">
      <v-list-subheader>Info</v-list-subheader>

      <v-list-item>
        <template v-slot:prepend>
          <v-icon :icon="'mdi-book'"></v-icon>
        </template>
        Rules
      </v-list-item>

      <v-list-item>
        <template v-slot:prepend>
          <v-icon :icon="'mdi-information'"></v-icon>
        </template>
        About D11
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script setup>
import { computed, ref } from "vue";
import { useDisplay } from "vuetify";

const drawer = ref(false);
const { xs } = useDisplay();

const density = computed(() => (xs.value ? "comfortable" : "default"));

function toggleDrawer() {
  drawer.value = !drawer.value;
}
</script>

<style scoped>
.d11-logo {
  margin-right: 64px;
}

.v-list-subheader {
  /* No variable for this */
  text-transform: uppercase;
}
</style>
