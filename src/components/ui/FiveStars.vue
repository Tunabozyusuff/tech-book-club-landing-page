<script setup lang="ts"></script>

<template>
  <div class="stars">
    <img
      v-for="n in 5"
      :key="n"
      src="/images/icon-star.svg"
      alt="star"
      width="20"
      height="20"
    />
  </div>
</template>

<style scoped>
.stars {
  display: flex;
  gap: 4px;
  align-items: center;
}

img {
  display: block;
}
</style>
