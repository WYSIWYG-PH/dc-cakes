<template>
    <div class="min-h-screen bg-white mt-10">
      
        <div class="text-center max-w-4xl mx-auto px-6">
            <h1 class="text-4xl lg:text-5xl font-bold mb-4 leading-tight">
                <span class="bg-gradient-to-r from-amber-600 to-orange-600 bg-clip-text text-transparent">
                    What Our Customers Say
                </span>
            </h1>
            <p class="text-gray-600 text-lg">
                Real reviews from real customers. See why they love our cakes!
            </p>
            <div class="h-1 w-16 bg-amber-500 mx-auto rounded-full mt-4"></div>
        </div>

        <div class="max-w-7xl mx-auto px-6 py-14">
            <div v-if="images.length === 0" class="text-center py-20">
                <div class="inline-block animate-spin rounded-full h-12 w-12 border-b-2 border-amber-600"></div>
                <p class="mt-4 text-gray-600">Loading reviews...</p>
            </div>
            <div v-else class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                <div v-for="(image, index) in images" :key="index"
                    class="group relative min-h-[350px] rounded-xl overflow-hidden shadow-md hover:shadow-xl transition-all duration-300 cursor-pointer border-2 border-amber-400">

                    <img :src="image.src" :alt="image.alt"
                        class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
                        loading="lazy" />
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const images = computed(() => {
    return Array.from({ length: 29 }, (_, i) => {
        const num = 935 + i;
        return {
            src: `/images/reviews/IMG_${num.toString().padStart(4, '0')}.JPG`,
            alt: `Customer Review ${i + 1}`
        };
    });
});
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
    transition: opacity .3s ease;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}

.zoom-enter-active,
.zoom-leave-active {
    transition: transform .3s cubic-bezier(0.34, 1.56, 0.64, 1), opacity .3s ease;
}

.zoom-enter-from,
.zoom-leave-to {
    transform: scale(0.95);
    opacity: 0;
}
</style>