<template>
  <h1 class="text-4xl font-semibold text-center my-20">Themes developed by FuryBee</h1>

  <div class="container mx-auto">
    <div class="grid  lg:grid-cols-3 2xl:grid-cols-4 gap-6">
      <theme-card v-for="(theme, index) in themes" :key="index" :theme="theme"></theme-card>
    </div>
  </div>
</template>

<style scoped></style>
<script setup lang="ts">
import ThemeCard from './components/ThemeCard.vue';

const themes = [
  {
    name: 'FuryDim',
    description: 'Embrace the perfect balance of dark elegance and soothing comfort.',
    link: 'https://chromewebstore.google.com/detail/furydim/mgfflkaaminidicgiamclancbbddmkhd',
    miniature: 'themes/FuryDim/miniature.png',
    icon: 'themes/FuryDim/icon.png',
  },
  {
    name: 'FuryAqua',
    description: 'Dive into the refreshing depths of sleek design and oceanic tranquility.',
    link: 'https://chromewebstore.google.com/detail/furyaqua/eiccbleglgobgdnneemdfhcpmejlpjjj',
    miniature: 'themes/FuryAqua/miniature.png',
    icon: 'themes/FuryAqua/icon.png',
  },
  {
    name: 'FuryLemonade',
    description: 'Refresh your browsing experience with zesty vibes and sunny design.',
    link: 'https://chromewebstore.google.com/detail/furylemonade/dedjpfknphaahjppdigngnhccgehcnai',
    miniature: 'themes/FuryLemonade/miniature.png',
    icon: 'themes/FuryLemonade/icon.png',
  },
  {
    name: 'FuryValentine',
    description: 'Surround yourself with the warmth of love and romantic charm.',
    link: 'https://chromewebstore.google.com/detail/mckmpfmadoendlbahlmbpnnldekajkbm',
    miniature: 'themes/FuryValentine/miniature.png',
    icon: 'themes/FuryValentine/icon.png',
  },
  {
    name: 'FuryCupcake',
    description: 'Indulge in a sweet blend of playful charm and delightful design.',
    link: 'https://chromewebstore.google.com/detail/furycupcake/ckngjhpmfmaceefpidpciedmoglldcom',
    miniature: 'themes/FuryCupcake/miniature.png',
    icon: 'themes/FuryCupcake/icon.png',
  },
];
</script>
