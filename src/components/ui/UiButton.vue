<script setup lang="ts">
defineProps<{
  buttonText?: string;
}>();
</script>
<template>
  <a href="#" class="text-6 btn">{{ buttonText }}</a>
</template>

<style lang="scss" scoped></style>
