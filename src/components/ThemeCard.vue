<template>
  <a :href="props.theme.link" target="_blank">
    <div class="rounded-2xl bg-stone-100 hover:bg-stone-200">
      <div class="p-4 pb-0">
        <img :src="props.theme.miniature" class="rounded-xl w-full" alt="FuryDim Miniature">
      </div>
      <div class="flex mt-2">
        <img :src="props.theme.icon" class="rounded-xl h-20 pl-1" alt="FuryDim Logo">
        <div class="flex flex-col justify-items-start items-start pt-2">
          <h2 class="font-semibold">{{ props.theme.name }}</h2>
          <p class="text-sm pt-0">{{ props.theme.description }}</p>
        </div>
      </div>
    </div>
  </a>
</template>
<script setup lang="ts">
type Theme = {
  name: string,
  description: string,
  link: string,
  miniature: string,
  icon: string,
};

const props = defineProps<{
  theme: Theme,
}>();
</script>
