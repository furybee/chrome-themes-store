<template>
  <a :href="props.item.link" target="_blank">
    <div class="flex rounded-2xl bg-stone-100 hover:bg-stone-200" :class="mode === 'row' ? 'xl:flex-row flex-col' : 'flex-col'">
      <div class="flex-0 p-4 pb-0">
        <img :src="props.item.miniature" class="rounded-xl" :class="mode === 'row' ? 'xl:max-w-xl' : 'w-full'" alt="FuryDim Miniature">
      </div>
      <div class="flex flex-1 mt-2" :class="mode === 'row' ? 'p-4' : 'pb-2'">
        <img v-if="mode === 'col'" :src="props.item.icon" class="rounded-xl h-20 pl-1" alt="FuryDim Logo">
        <div class="flex flex-col justify-items-start items-start pt-2">
          <h2 class="font-semibold" :class="{ 'flex items-center gap-2 mb-4': mode === 'row'}">
            <img v-if="mode === 'row'" :src="props.item.icon" class="h-8 pl-1 " alt="FuryDim Logo">
            {{ props.item.name }}
          </h2>
          <p class="text-sm pt-0 pr-2" v-html="props.item.description"></p>
        </div>
      </div>
    </div>
  </a>
</template>
<script setup lang="ts">
type FuryCardItem = {
  name: string,
  description: string,
  link: string,
  miniature: string,
  icon: string,
};

const props = withDefaults(defineProps<{
  item: FuryCardItem,
  mode: string
}>(), {
  mode: 'col'
})
</script>
