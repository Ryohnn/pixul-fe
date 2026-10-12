<script setup lang="ts">
type LinkItemType = "logo" | "button" | "standard";

interface LinkItemProps {
  href: string;
  type?: LinkItemType;
}

const { href, type = "button" } = defineProps<LinkItemProps>();
</script>

<template>
  <a :href="href" class="link" :class="type">
    <slot></slot>
  </a>
</template>

<style scoped lang="scss">
.link {
  text-decoration: none;
  color: white;
  transition: 0.4s;

  &.logo {
    height: 100%;
    :slotted(img) {
      height: 100%;
    }
  }

  &.button {
    border: 1px solid grey;
    border-radius: 0.35rem;
    padding: 0.25rem;
  }
}

@media (hover: hover) {
  .link:hover {
    opacity: 0.5;

    &.button {
      opacity: 1;
      background: #424242;
    }
  }
}
</style>
