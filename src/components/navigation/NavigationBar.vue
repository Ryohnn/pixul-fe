<script setup lang="ts">
import LinkItem from "@/components/navigation/LinkItem.vue";
</script>

<template>
  <nav class="navbar top">
    <div class="left-group">
      <LinkItem href="/" type="logo">
        <img alt="Vue logo" src="@/assets/pixul-logo.svg" />
      </LinkItem>

      <LinkItem href="/counter">
        <p>Counter</p>
      </LinkItem>

      <LinkItem href="/games">
        <p>Game List</p>
      </LinkItem>

      <LinkItem href="/admin/games">
        <p>Manage Games</p>
      </LinkItem>
    </div>
  </nav>
</template>

<style scoped lang="scss">
.navbar {
  height: 100%;
}

.navbar .left-group {
  height: 100%;
  display: flex;
  align-items: center;
}
</style>
