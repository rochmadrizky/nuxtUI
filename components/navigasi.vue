<template>
  <ul class="flex flex-col lg:flex-row lg:space-x-7">
    <li class="mb-8 ml-3 lg:mb-0">
      <NuxtLink
        to="/"
        @click="$emit(`onMenuClick`)"
        class="font-first md:text-xl"
        >Wellcome!</NuxtLink
      >
    </li>
  </ul>
</template>

<script setup>
defineEmits(["onMenuClick"]);
</script>
