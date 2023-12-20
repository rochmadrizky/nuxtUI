<template>
  <header class="bg-gray-100 p-2 sticky top-0 left-0 right-0 z-10">
    <div
      class="container md:px-20 mx-auto flex justify-between items-center lg:flex-col"
    >
      <div class="text-2xl font-bold mb-2">I say hello</div>

      <button @click="toggleMenu" class="lg:hidden relative ml-60 z-50">
        <component :is="isSidebarOpen ? IconX : IconMenu2"></component>
      </button>

      <div
        v-if="isSidebarOpen"
        @click="toggleMenu"
        class="fixed inset-0 bg-black opacity-10 z-40"
      ></div>

      <div :class="sidebarClasses">
        <div class="py-6">
          <a href="#" class="text-2xl font-bold mb-2">I say hello</a>
        </div>
        <Navigasi @onMenuClick="() => (isSidebarOpen = false)" />
      </div>

      <div class="hidden lg:block">
        <Navigasi />
      </div>
    </div>
  </header>
</template>

<script setup>
import { IconMenu2 } from "@tabler/icons-vue";
import { IconX } from "@tabler/icons-vue";
import Navigasi from "./navigasi.vue";
import { ref, computed } from "vue";

const isSidebarOpen = ref(false);

const toggleMenu = () => {
  isSidebarOpen.value = !isSidebarOpen.value;
};

const sidebarClasses = computed(() => {
  return (
    "fixed top-0 left-0 h-full w-64 md:w-72 lg:w-[600px] bg-gray-100 text-black px-4 transform transition-transform duration-300 ease-in-out z-50" +
    (isSidebarOpen.value ? " translate-x-0" : " -translate-x-full")
  );
});
</script>
