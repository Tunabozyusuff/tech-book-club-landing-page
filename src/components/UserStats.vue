<script setup lang="ts">
import FiveStars from "./ui/FiveStars.vue";
</script>

<template>
  <aside class="user-stats">
    <div class="user-stats-layout">
      <img
        src="/images/image-avatars.webp"
        alt="User Avatars"
        width="110"
        height="40"
      />
      <div class="user-stats-content">
        <FiveStars />

        <p class="text-preset-7">200+ developers joined already</p>
      </div>
    </div>
  </aside>
</template>

<style scoped>
.user-stats {
  margin-top: var(--spacing-20);

  .user-stats-layout {
    display: flex;
    align-items: center;
    gap: var(--spacing-12);
  }
}
</style>
