<script setup lang="ts">
defineProps<{
  buttonText?: string;
  icon?: "arrow-down" | "arrow-up";
}>();
</script>
<template>
  <a
    href="#"
    class="text-preset-6 btn"
    :class="{
      'btn-icon': icon,
      'btn-icon icon-arrow-down': icon === 'arrow-down',
      'btn-icon icon-arrow-up': icon === 'arrow-up',
    }"
  >
    {{ buttonText }}</a
  >
</template>

<style lang="scss" scoped>
.btn {
  display: inline-block;
  margin-top: var(--spacing-400); // 32px boşluk
  font-family: var(--ff-martian-mono);
  color: var(--clr-neutral-900);
  border: 2px solid var(--clr-neutral-900);
  border-radius: var(--radius-8);
  padding: var(--spacing-20) var(--spacing-24);
  background-color: var(--clr-light-salmon-50);
  background-repeat: no-repeat;
  background-position: right var(--spacing-24) center;
}

.btn-icon {
  padding-right: var(--spacing-64);
}

.icon-arrow-down {
  background-image: url("/images/icon-arrow-down.svg");
}

.icon-arrow-up {
  background-image: url("/images/icon-arrow-up.svg");
  border-color: var(--clr-neutral-0);
  background-color: transparent;
  color: var(--clr-neutral-0);
}
</style>
