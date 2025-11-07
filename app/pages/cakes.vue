<template>
  <Title>Our Cakes — DC Cakes</Title>

  <section class="py-16 bg-white">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl text-center relative">
  <NuxtLink to="/" aria-label="Back to home" class="hidden lg:flex fixed left-24 top-28 p-3 text-amber-600 bg-white/95 hover:bg-amber-50 rounded-full z-50 shadow-md border border-amber-200 transition-colors duration-150 focus:outline-none focus-visible:ring-2 focus-visible:ring-amber-400">
          <span class="sr-only">Back to Home</span>
          <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
            <path fill-rule="evenodd" d="M12.707 14.707a1 1 0 01-1.414 0L6.586 10l4.707-4.707a1 1 0 011.414 1.414L9.414 10l3.293 3.293a1 1 0 010 1.414z" clip-rule="evenodd" />
          </svg>
        </NuxtLink>
        <h1 class="text-4xl font-bold text-amber-600 sm:text-5xl">Our Cakes</h1>
        <p class="mt-4 text-lg text-[#6B5D4F]">Browse our signature cakes and custom creations — handcrafted for every celebration.</p>
      </div>

      <div class="mx-auto mt-12 grid max-w-2xl grid-cols-1 gap-8 sm:mt-16 sm:grid-cols-2 lg:mx-0 lg:max-w-none lg:grid-cols-3">
        <article v-for="cake in cakes" :key="cake.name" class="flex flex-col items-start rounded-2xl overflow-hidden shadow-lg bg-white">
          <div class="relative w-full overflow-hidden">
            <img :src="cake.image" :alt="cake.name" class="aspect-[16/9] w-full object-cover" />
          </div>
          <div class="p-6 w-full">
            <h3 class="text-xl font-semibold leading-6" style="color: #4A3B2B;">{{ cake.name }}</h3>
            <p class="mt-3 text-sm leading-6" style="color: #6B5D4F;">{{ cake.description }}</p>
            <div class="mt-4 flex items-center justify-between w-full">
              <div class="text-amber-600 font-semibold">{{ cake.price }}</div>
              <NuxtLink :to="`/order?cake=${encodeURIComponent(cake.name)}`" class="rounded-full bg-amber-600 px-3 py-2 text-sm font-semibold text-white shadow hover:bg-amber-700">Order</NuxtLink>
            </div>
          </div>
        </article>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const cakes = ref([
  {
    name: 'Chocolate Dream',
    description: 'Rich layers of chocolate cake with velvety ganache frosting and gold leaf accents.',
    image: 'https://images.unsplash.com/photo-1578985545062-69928b1d9587?w=1200&q=80',
    price: '₱1,800'
  },
  {
    name: 'Vanilla Rose Elegance',
    description: 'Classic vanilla sponge with Swiss meringue buttercream and handcrafted sugar roses.',
    image: 'https://images.unsplash.com/photo-1464349095431-e9a21285b5f3?w=1200&q=80',
    price: '₱1,600'
  },
  {
    name: 'Red Velvet Delight',
    description: 'Luxurious red velvet layers with cream cheese frosting and white chocolate drizzle.',
    image: 'https://images.unsplash.com/photo-1606890737304-57a1ca8a5b62?w=1200&q=80',
    price: '₱1,700'
  },
  {
    name: 'Lemon Blossom',
    description: 'Bright lemon sponge with lemon curd and light buttercream, perfect for springtime events.',
    image: 'https://images.unsplash.com/photo-1551024601-bec78aea704b?w=1200&q=80',
    price: '₱1,500'
  },
  {
    name: 'Salted Caramel Indulgence',
    description: 'Salted caramel layers with caramel buttercream and crunchy toffee bits.',
    image: 'https://images.unsplash.com/photo-1604147706287-9a9d1d0e0b7b?w=1200&q=80',
    price: '₱1,900'
  },
  {
    name: 'Matcha Mousse',
    description: 'Delicate matcha sponge with light matcha mousse and white chocolate accents.',
    image: 'https://images.unsplash.com/photo-1547592166-8b3b8ec6b16b?w=1200&q=80',
    price: '₱1,850'
  },
])
</script>

<style scoped>
.cake-grid {
  display: grid;
}
</style>
