<template>
  <a href="https://github.com/furybee" target="_blank" class="text-yellow-600 hover:text-yellow-700 absolute top-5 right-5 "><GithubIcon class="inline h-8 xl:h-12"/></a>

  <h1 class="text-3xl xl:text-5xl font-semibold text-center mt-20 mb-8 xl:mb-20">Fury<span class="text-yellow-500">Bee</span> Web Store</h1>

  <div class="container mx-auto pb-44 p-2 xl:p-0">
    <h2 class="text-2xl xl:text-4xl font-semibold text-center my-8 xl:my-20">Explore Our themes</h2>

    <div class="grid  lg:grid-cols-3 2xl:grid-cols-4 gap-6">
      <FuryCard v-for="(theme, index) in themes" :key="index" :item="theme" mode="col"></FuryCard>
    </div>


    <h2 class="text-2xl xl:text-4xl font-semibold text-center my-8 mt-32 xl:my-20">Discover our extensions</h2>
      <div>
        <FuryCard v-for="(extension, index) in extensions" :key="index" :item="extension" mode="row"></FuryCard>
      </div>
  </div>

  <footer class="bg-stone-100 text-center py-4 mt-20">
    <p class="text-sm">
      © {{ (new Date()).getFullYear() }} FuryBee.
      All rights reserved.
      Made with ❤️ by <a href="https://github.com/furybee" target="_blank" class="text-yellow-600 hover:text-yellow-700">FuryBee</a>.
    </p>
  </footer>
</template>

<style scoped></style>
<script setup lang="ts">
import FuryCard from './components/FuryCard.vue';
import GithubIcon from "./icons/GithubIcon.vue";

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
  // {
  //   name: "FuryRetro",
  //   description: "Indulge in a sweet blend of playful charm and delightful design.",
  //   link: "https://chromewebstore.google.com/detail/_________THEME_ID_________",
  //   miniature: "themes/FuryRetro/miniature.png",
  //   icon: "themes/FuryRetro/icon.png",
  // }
];

const extensions = [
  {
    name: 'Tab Modifier - Take control of your tabs',
    description: `Take full control of your tabs with our extension:

- Rename tabs for <strong>perfect organization</strong>
- Customize tab icons for visual navigation
- Pin important tabs for quick access
- Group tabs according to your needs for <strong>efficient management</strong>
- Prevent accidental closure of essential tabs
- Make each tab <strong>unique</strong> for personalized browsing
- <strong>Mute noisy tabs</strong> for uninterrupted browsing experience
- Set your preferences directly from the options page for complete customization.

And don't forget: our extension is open-source! Contribute now on GitHub to enhance your browsing experience.

Take full control of your browsing experience with our extension and discover a new way to manage tabs effectively and tailored to your preferences.`.replace(/\n/g, '<br>'),
    link: 'https://chromewebstore.google.com/detail/tab-modifier/hcbgadmbdkiilgpifjgcakjehmafcjai',
    miniature: 'extensions/TabModifier/miniature.png',
    icon: 'extensions/TabModifier/icon.png',
  },
];
</script>
