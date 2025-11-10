<template>
  <Title>DC Cakes</Title>

  <section class="py-16 bg-white">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl text-center relative">
        <NuxtLink
          to="/"
          aria-label="Back to home"
          class="hidden lg:flex fixed left-24 top-28 p-3 text-amber-600 bg-white/95 hover:bg-amber-50 rounded-full z-50 shadow-md border border-amber-200 transition-colors duration-150 focus:outline-none focus-visible:ring-2 focus-visible:ring-amber-400"
        >
          <span class="sr-only">Back to Home</span>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-8 w-8"
            viewBox="0 0 20 20"
            fill="currentColor"
            aria-hidden="true"
          >
            <path
              fill-rule="evenodd"
              d="M12.707 14.707a1 1 0 01-1.414 0L6.586 10l4.707-4.707a1 1 0 011.414 1.414L9.414 10l3.293 3.293a1 1 0 010 1.414z"
              clip-rule="evenodd"
            />
          </svg>
        </NuxtLink>
        <h1 class="text-4xl font-bold text-amber-600 sm:text-5xl">Our Cakes</h1>
        <p class="mt-4 text-lg text-[#6B5D4F]">
          Browse our signature cakes and custom creations handcrafted for every
          celebration.
        </p>
      </div>

      <div class="mt-8 flex flex-col gap-4 sm:flex-row sm:items-center sm:justify-between">
        <div class="relative w-full sm:max-w-md">
          <label for="search" class="sr-only">Search cakes</label>
          <input
            id="search"
            v-model="searchQuery"
            type="search"
            placeholder="Search cakes..."
            class="w-full rounded-md border border-transparent bg-amber-600 px-3 py-2 text-sm text-white shadow-md placeholder:text-white/80 focus:outline-none focus-visible:ring-2 focus-visible:ring-amber-300 focus:border-amber-100 hover:bg-amber-500 transition-colors"
          />
        </div>
        <div class="relative w-full sm:w-auto">
          <label for="category" class="sr-only">Category</label>
          <select
            id="category"
            v-model="selectedCategory"
            class="appearance-none text-center w-48 rounded-md border border-transparent bg-amber-600 px-3 py-2 pr-8 text-sm text-white shadow-md hover:bg-amber-500 focus:outline-none focus-visible:ring-2 focus-visible:ring-amber-300 transition-colors"
          >
            <option value="">All Categories</option>
            <option v-for="cat in categories" :key="cat" :value="cat">
              {{ cat }}
            </option>
          </select>
          <svg
            class="pointer-events-none absolute right-2 top-1/2 h-4 w-4 -translate-y-1/2 text-white"
            viewBox="0 0 20 20"
            fill="none"
            stroke="currentColor"
            stroke-width="1.5"
            aria-hidden="true"
          >
            <path
              d="M6 8l4 4 4-4"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </div>
      </div>

      <div
        class="mx-auto mt-12 grid max-w-2xl grid-cols-1 gap-8 sm:mt-16 sm:grid-cols-2 lg:mx-0 lg:max-w-none lg:grid-cols-3"
      >
        <article
          v-for="cake in filteredCakes"
          :key="cake.name"
          class="flex flex-col items-start rounded-2xl overflow-hidden shadow-lg bg-white"
        >
          <div class="relative w-full overflow-hidden">
            <img
              :src="cake.images[0]"
              :alt="cake.name"
              class="w-full aspect-square object-cover cursor-pointer transition-transform duration-300 hover:scale-105"
              @click="openImageViewer(cake, 0)"
            />
          </div>
          <div class="p-6 w-full">
            <h3 class="text-xl font-semibold leading-6" style="color: #4a3b2b">
              {{ cake.name }}
            </h3>
            <p class="mt-3 text-sm leading-6" style="color: #6b5d4f">
              {{ cake.description }}
            </p>
            <div class="mt-4 flex items-center justify-between w-full">
              <div class="text-amber-600 font-semibold">{{ cake.price }}</div>
            </div>
          </div>
        </article>
      </div>
    </div>

    <div v-if="isViewerOpen" class="fixed inset-0 z-50 flex items-center justify-center bg-black bg-opacity-90">
      <button @click="closeImageViewer" class="absolute top-4 right-4 text-white hover:text-amber-200">
        <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
      
      <button @click="previousImage" class="absolute left-4 text-white hover:text-amber-200">
        <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
        </svg>
      </button>

      <img 
        v-if="currentImageSet" 
        :src="currentImageSet[currentImageIndex]" 
        class="max-h-[90vh] max-w-[90vw] object-contain"
        alt="Enlarged cake image"
      />

      <button @click="nextImage" class="absolute right-4 text-white hover:text-amber-200">
        <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
        </svg>
      </button>
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from "vue";
import cakesData from "/data/cake.js";

const cakes = ref(cakesData);

// Derive categories from the actual cake data
const categories = computed(() => {
  const uniqueCategories = new Set(cakes.value.map(cake => cake.category));
  return Array.from(uniqueCategories).sort();
});

const selectedCategory = ref("");
const searchQuery = ref("");

const filteredCakes = computed(() => {
  const query = searchQuery.value.trim().toLowerCase();

  return cakes.value.filter((cake) => {
    const matchesCategory =
      !selectedCategory.value || cake.category === selectedCategory.value;
    const matchesSearch =
      !query ||
      cake.name.toLowerCase().includes(query) ||
      (cake.description && cake.description.toLowerCase().includes(query));

    return matchesCategory && matchesSearch;
  });
});

const currentImageSet = ref(null);
const currentImageIndex = ref(0);
const isViewerOpen = ref(false);

function openImageViewer(cake, index) {
  currentImageSet.value = cake.images;
  currentImageIndex.value = index;
  isViewerOpen.value = true;
}

function closeImageViewer() {
  isViewerOpen.value = false;
}

function nextImage() {
  if (currentImageSet.value) {
    currentImageIndex.value = (currentImageIndex.value + 1) % currentImageSet.value.length;
  }
}

function previousImage() {
  if (currentImageSet.value) {
    currentImageIndex.value = currentImageIndex.value === 0 
      ? currentImageSet.value.length - 1 
      : currentImageIndex.value - 1;
  }
}
</script>

<style scoped>
.cake-grid {
  display: grid;
}
</style>
