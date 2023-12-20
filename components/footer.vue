<template>
  <div class="py-4 bg-gray-100 bottom-0">
    <div class="text-center">
      <p>&copy;{{ Tahun }} All rights reserved.</p>
    </div>
  </div>
</template>

<script setup>
const Tahun = new Date().getFullYear();
</script>
