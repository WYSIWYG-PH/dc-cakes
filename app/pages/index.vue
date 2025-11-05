<template>
  <Title>DC Cakes</Title>
  <!-- Hero Section -->
  <section class="relative isolate overflow-hidden bg-white">
    <!-- Animated background pattern -->
    <svg
      class="absolute inset-0 -z-10 size-full mask-[radial-gradient(100%_100%_at_top_right,white,transparent)] stroke-amber-200"
      aria-hidden="true">
      <defs>
        <pattern id="cake-pattern" width="200" height="200" x="50%" y="-1" patternUnits="userSpaceOnUse">
          <path d="M.5 200V.5H200" fill="none" />
        </pattern>
      </defs>
      <svg x="50%" y="-1" class="overflow-visible fill-amber-50">
        <path d="M-200 0h201v201h-201Z M600 0h201v201h-201Z M-400 600h201v201h-201Z M200 800h201v201h-201Z"
          stroke-width="0" />
      </svg>
      <rect width="100%" height="100%" stroke-width="0" fill="url(#cake-pattern)" />
    </svg>

    <!-- Decorative elements -->
    <div
      class="absolute top-10 left-[calc(50%-4rem)] -z-10 transform-gpu blur-3xl sm:left-[calc(50%-18rem)] lg:top-[calc(50%-30rem)] lg:left-48 xl:left-[calc(50%-24rem)]"
      aria-hidden="true">
      <div class="aspect-[1108/632] w-[69.25rem] bg-amber-400 opacity-10"
        style="clip-path: polygon(73.6% 51.7%, 91.7% 11.8%, 100% 46.4%, 97.4% 82.2%, 92.5% 84.9%, 75.7% 64%, 55.3% 47.5%, 46.5% 49.4%, 45% 62.9%, 50.3% 87.2%, 21.3% 64.1%, 0.1% 100%, 5.4% 51.1%, 21.4% 63.9%, 58.9% 0.2%, 73.6% 51.7%)">
      </div>
    </div>

    <div class="absolute top-[40%] right-[10%] -z-10 transform-gpu blur-3xl" aria-hidden="true">
      <div class="aspect-[1108/632] w-[50rem] bg-yellow-300 opacity-8"
        style="clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%)">
      </div>
    </div>

    <div class="mx-auto max-w-7xl px-6 pt-10 pb-24 sm:pb-32 lg:flex lg:px-8 lg:py-40">
      <div class="mx-auto max-w-2xl shrink-0 lg:mx-0 lg:pt-8">
        <div class="flex items-center gap-3">
          <img src="/images/logo.jpg" alt="DC Cakes Logo" class="w-14 h-14 object-cover rounded-full" />
          <div class="text-4xl font-bold bg-[#4A3B2B] bg-clip-text text-transparent">
            DC Cakes
          </div>
        </div>
        <h1 class="mt-10 text-5xl font-bold tracking-tight text-pretty text-[#4A3B2B] sm:text-7xl">
          Handcrafted Cakes That Make
          <span class="text-amber-600">
            Celebrations Unforgettable
          </span>
        </h1>
        <p class="mt-8 text-lg font-medium text-pretty text-[#4A3B2B] sm:text-xl/8">
          From elegant wedding cakes to whimsical birthday treats, every creation is baked fresh with premium
          ingredients and decorated with love. Your dream cake awaits.
        </p>
        <div class="mt-12 flex items-center gap-8 text-md text-gray-700 font-medium">
          <div class="flex items-center gap-2">
            <Icon name="ph:check-circle-fill" class="w-10 h-10 text-amber-600" />
            <span>Fresh Daily</span>
          </div>

          <div class="flex items-center gap-2">
            <Icon name="ph:check-circle-fill" class="w-10 h-10 text-amber-600" />
            <span>Custom Designs</span>
          </div>

          <div class="flex items-center gap-2">
            <Icon name="ph:check-circle-fill" class="w-10 h-10 text-amber-600" />
            <span>Same-Day Delivery</span>
          </div>
        </div>
      </div>
      <div class="mx-auto mt-16 flex max-w-2xl sm:mt-24 lg:mt-0 lg:mr-0 lg:ml-10 lg:max-w-none lg:flex-none xl:ml-32">
        <div class="max-w-3xl flex-none sm:max-w-5xl lg:max-w-none">
          <div class="relative">
            <img src="https://images.unsplash.com/photo-1578985545062-69928b1d9587?w=1200&q=80"
              alt="Beautifully decorated DC Cakes signature cake" width="2432" height="1442"
              class="w-[76rem] rounded-2xl bg-white shadow-2xl ring-1 ring-gray-900/10" />
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Top Sellers Section -->
  <section class="py-24 sm:py-32" style="background-color: #f6f5f3;">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-3xl font-bold text-amber-600 tracking-tight sm:text-4xl">Our Top Sellers</h2>
        <p class="mt-4 text-lg" style="color: #6B5D4F;">
          Discover our most loved creations, crafted with passion and perfection
        </p>
      </div>

      <div
        class="mx-auto mt-16 grid max-w-2xl grid-cols-1 gap-x-8 gap-y-12 sm:mt-20 lg:mx-0 lg:max-w-none lg:grid-cols-3">
        <!-- Cake 1 -->
        <article class="flex flex-col items-start rounded-2xl overflow-hidden shadow-lg"
          style="background-color: white;">
          <div class="relative w-full overflow-hidden">
            <img src="https://images.unsplash.com/photo-1578985545062-69928b1d9587?w=800&q=80"
              alt="Chocolate Dream Cake" class="aspect-[16/9] w-full object-cover" />
          </div>
          <div class="p-6 w-full">
            <div class="group relative mt-3">
              <h3 class="text-xl font-semibold leading-6" style="color: #4A3B2B;">
                Chocolate Dream
              </h3>
              <p class="mt-3 text-sm leading-6" style="color: #6B5D4F;">
                Rich layers of chocolate cake with velvety ganache frosting, topped with chocolate shavings and gold
                leaf accents.
              </p>
            </div>
          </div>
        </article>

        <!-- Cake 2 -->
        <article class="flex flex-col items-start rounded-2xl overflow-hidden shadow-lg"
          style="background-color: white;">
          <div class="relative w-full overflow-hidden">
            <img src="https://images.unsplash.com/photo-1464349095431-e9a21285b5f3?w=800&q=80"
              alt="Vanilla Rose Elegance Cake" class="aspect-[16/9] w-full object-cover" />
            <div class="absolute top-4 right-4 rounded-full px-3 py-1 text-xs font-semibold text-white"
              style="background-color: #D4AF37;">
              Best Seller
            </div>
          </div>
          <div class="p-6 w-full">
            <div class="group relative mt-3">
              <h3 class="text-xl font-semibold leading-6" style="color: #4A3B2B;">
                Vanilla Rose Elegance
              </h3>
              <p class="mt-3 text-sm leading-6" style="color: #6B5D4F;">
                Classic vanilla sponge with Swiss meringue buttercream, adorned with handcrafted sugar roses.
              </p>
            </div>
          </div>
        </article>

        <!-- Cake 3 -->
        <article class="flex flex-col items-start rounded-2xl overflow-hidden shadow-lg"
          style="background-color: white;">
          <div class="relative w-full overflow-hidden">
            <img src="https://images.unsplash.com/photo-1606890737304-57a1ca8a5b62?w=800&q=80"
              alt="Red Velvet Delight Cake" class="aspect-[16/9] w-full object-cover" />
          </div>
          <div class="p-6 w-full">
            <div class="group relative mt-3">
              <h3 class="text-xl font-semibold leading-6" style="color: #4A3B2B;">
                Red Velvet Delight
              </h3>
              <p class="mt-3 text-sm leading-6" style="color: #6B5D4F;">
                Luxurious red velvet layers with cream cheese frosting, finished with white chocolate drizzle.
              </p>
            </div>
          </div>
        </article>
      </div>
      <div class="mt-16 text-center">
        <a href="#"
          class="rounded-full bg-amber-600 px-6 py-3.5 text-sm font-semibold text-white shadow-lg hover:bg-gray-800 hover:shadow-xl hover:scale-105 transition-all duration-300 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-black">
          See All Our Sweet Creations 🍰
        </a>
      </div>
    </div>
  </section>

  <!-- Testimonials Section -->
  <section class="relative isolate overflow-hidden bg-white px-6 py-24 sm:py-32 lg:px-8">
    <div
      class="absolute inset-0 -z-10 bg-[radial-gradient(45rem_50rem_at_top,var(--color-amber-300),white)] opacity-20">
    </div>
    <div
      class="absolute inset-y-0 right-1/2 -z-10 mr-16 w-[200%] origin-bottom-left skew-x-[-30deg] bg-white shadow-xl ring-1 shadow-indigo-600/10 ring-indigo-50 sm:mr-28 lg:mr-0 xl:mr-16 xl:origin-center">
    </div>
    <div class="mx-auto max-w-2xl lg:max-w-4xl text-center">
      <h2 class="text-2xl font-bold text-amber-600">Testimonial</h2>
      <figure class="mt-10">
        <blockquote class="text-center text-xl/8 font-semibold text-[#4A3B2B] sm:text-2xl/9">
          <p>“The chocolate mousse cake was absolutely heavenly! The texture was light, the sweetness perfectly
            balanced, and it melted in my mouth. It’s honestly the best cake I’ve ever tasted!”</p>
        </blockquote>
        <figcaption class="mt-10">
          <img class="mx-auto size-10 rounded-full"
            src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?...q=80" alt="" />
          <div class="mt-4 flex items-center justify-center space-x-3 text-base">
            <div class="font-semibold text-[#4A3B2B]">Jane Doe</div>
          </div>
        </figcaption>
      </figure>
    </div>
  </section>

  <footer class="relative overflow-hidden" style="background-color: #4A3B2B;">
    <div class="absolute top-0 left-0 right-0 h-1" style="background-color: #D4AF37;"></div>
    <div class="absolute inset-0 opacity-5">
      <svg class="h-full w-full" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <pattern id="footer-pattern" x="0" y="0" width="80" height="80" patternUnits="userSpaceOnUse">
            <circle cx="40" cy="40" r="1.5" fill="white" />
          </pattern>
        </defs>
        <rect width="100%" height="100%" fill="url(#footer-pattern)" />
      </svg>
    </div>

    <div class="relative mx-auto max-w-7xl px-6 py-16 lg:px-8">
      <div class="grid grid-cols-1 gap-12 md:grid-cols-2 lg:grid-cols-4">
        <div class="lg:col-span-1">
          <div class="flex items-center gap-3 mb-6">
            <img src="/images/logo.jpg" alt="DC Cakes Logo" class="w-12 h-12 object-cover rounded-full ring-2 ring-[#D4AF37]"
              style="ring-color: #D4AF37;" />
            <div class="text-2xl font-bold text-white">DC Cakes</div>
          </div>
          <p class="text-sm text-white/80 leading-relaxed">
            Crafting sweet memories with every bite. Premium cakes made fresh daily with love and the finest
            ingredients.
          </p>
        </div>
        <div>
          <h3 class="text-sm font-semibold text-white mb-6">Follow Us</h3>
          <div class="flex gap-4">
            <a v-for="item in navigation.social" :key="item.name" :href="item.href" class="group">
              <div
                class="flex items-center justify-center w-12 h-12 rounded-full transition-all duration-300 hover:scale-110"
                style="background-color: rgba(212, 175, 55, 0.2);"
                @mouseenter="$event.currentTarget.style.backgroundColor = '#D4AF37'"
                @mouseleave="$event.currentTarget.style.backgroundColor = 'rgba(212, 175, 55, 0.2)'">
                <component :is="item.icon" class="w-6 h-6 text-white" aria-hidden="true" />
              </div>
              <span class="sr-only">{{ item.name }}</span>
            </a>
          </div>
        </div>
        <div class="lg:col-span-2">
          <h3 class="text-sm font-semibold text-white mb-6">Get In Touch</h3>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div class="flex items-start gap-3">
              <div class="flex items-center justify-center w-12 h-12 rounded-lg flex-shrink-0"
                style="background-color: rgba(212, 175, 55, 0.2);">
                <Icon name="ph:map-pin-bold" class="size-6" style="color: #D4AF37;" />
              </div>
              <div>
                <p class="text-sm font-semibold text-white mb-1">Location</p>
                <p class="text-sm text-white/70">123 Baker Street<br />Makati City, Metro Manila</p>
              </div>
            </div>
            <div class="flex items-start gap-3">
              <div class="flex items-center justify-center w-12 h-12 rounded-lg flex-shrink-0"
                style="background-color: rgba(212, 175, 55, 0.2);">
                <Icon name="ph:phone-bold" class="size-6" style="color: #D4AF37;" />
              </div>
              <div>
                <p class="text-sm font-semibold text-white mb-1">Phone</p>
                <p class="text-sm text-white/70">+63 (917) 123-4567</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="mt-12 pt-8 border-t border-white/10">
        <div class="flex flex-col md:flex-row justify-between items-center gap-4">
          <p class="text-sm text-white/60">
            &copy; 2025 DC Cakes. All rights reserved.
          </p>
        </div>
      </div>
    </div>
  </footer>

</template>

<script setup>
import { defineComponent, h } from 'vue'

const navigation = {
  social: [
    {
      name: 'Facebook',
      href: '#',
      icon: defineComponent({
        render: () =>
          h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
            h('path', {
              'fill-rule': 'evenodd',
              d: 'M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z',
              'clip-rule': 'evenodd',
            }),
          ]),
      }),
    },
    {
      name: 'Instagram',
      href: '#',
      icon: defineComponent({
        render: () =>
          h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
            h('path', {
              'fill-rule': 'evenodd',
              d: 'M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z',
              'clip-rule': 'evenodd',
            }),
          ]),
      }),
    },
  ],
}
</script>

<style scoped>
@keyframes float {

  0%,
  100% {
    transform: translateY(0px);
  }

  50% {
    transform: translateY(-10px);
  }
}

.hover\:scale-\[1\.02\]:hover {
  animation: float 3s ease-in-out infinite;
}
</style>