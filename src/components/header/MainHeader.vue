<script setup lang="ts">
import NavigationBar from "@/components/navigation/NavigationBar.vue";
</script>

<template>
  <header>
    <NavigationBar />
  </header>
</template>

<style scoped lang="scss">
header {
  padding: 1rem;
  height: 65px;
  position: sticky;
  top: 0;
  background-color: #222222;
}

@media (prefers-color-scheme: light) {
  header {
    background-color: white;
  }
}
</style>
