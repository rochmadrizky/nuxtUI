<template>
  <div class="container flex items-center justify-center">
    <div class="grid grid-cols-1 sm:grid-cols-1 lg:grid-cols-1 gap-8">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="max-w-sm rounded overflow-hidden shadow-lg"
      >
        <img
          :src="project.image"
          alt="Project Image"
          class="w-full h-48 object-cover"
        />
        <div class="px-6 py-2">
          <div class="font-bold text-xl mb-2">{{ project.title }}</div>
          <p class="text-gray-700 text-base">{{ project.description }}</p>
        </div>
        <div class="px-6 pt-2 pb-4 grid grid-cols-2 md:grid-cols-4 gap-2">
          <UBadge color="primary" variant="solid">Badge</UBadge>
          <UBadge color="rose" variant="solid">Badge</UBadge>
          <UBadge color="indigo" variant="solid">Badge</UBadge>
          <UBadge color="violet" variant="solid">Badge</UBadge>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const projects = ref([
  {
    title: "Project 1",
    description: "Description for project 1.",
    image: "https://placekitten.com/400/300",
  },
  {
    title: "Project 2",
    description: "Description for project 2.",
    image: "https://placekitten.com/401/300",
  },
  {
    title: "Project 3",
    description: "Description for project 3.",
    image: "https://placekitten.com/402/300",
  },
]);
</script>
