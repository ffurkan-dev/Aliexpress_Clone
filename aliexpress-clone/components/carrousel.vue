<template>
  <div class="relative w-full max-w-5xl mx-auto p-4 bg-white rounded-lg shadow-lg overflow-hidden">

    <div class="py-4 px-6 bg-yellow-200 rounded-lg">
      <h2 class="text-lg font-bold">Dollar Express</h2>
      <p class="text-sm">3 from $0.99</p>
    </div>

    <div class="relative mt-2 overflow-hidden">
      <button
        class="absolute left-2 top-1/2 transform -translate-y-1/2 z-10 p-2 bg-yellow-300 rounded-full shadow-md hover:bg-yellow-400"
        @click="prevSlide"
      >
        &lt;
      </button>

      <div
        class="flex transition-transform duration-300"
        :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
      >
        <div
          v-for="(item, index) in items"
          :key="index"
          class="w-1/4 flex-shrink-0 px-2 box-border"
        >
          <div
            class="bg-gray-100 p-4 rounded-lg shadow-md flex flex-col items-center h-full cursor-pointer hover:bg-gray-200 transition"
            @click="handleProductClick(item)"
          >
            <img
              :src="item.image"
              alt="Product"
              class="w-24 h-24 object-cover rounded-md mb-2"
            />
            <h3 class="text-sm font-semibold text-center mb-2">
              {{ item.name }}
            </h3>
            <div class="flex items-center space-x-2 mb-2">
              <p class="text-gray-500 text-xs line-through">{{ item.oldPrice }}</p>
              <p class="text-red-500 text-sm font-bold">{{ item.discountedPrice }}</p>
            </div>
            <p class="text-yellow-500 text-xs">{{ item.rating }} ★</p>
          </div>
        </div>
      </div>

      <button
        class="absolute right-2 top-1/2 transform -translate-y-1/2 z-10 p-2 bg-yellow-300 rounded-full shadow-md hover:bg-yellow-400"
        @click="nextSlide"
      >
        &gt;
      </button>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "Carousel",
  setup() {
    const items = ref([
      {
        name: "Table",
        oldPrice: "$13.29",
        discountedPrice: "$1.33",
        rating: 4.4,
        image: "https://ae-pic-a1.aliexpress-media.com/kf/S7fe61a03d3484d249a2d527a5d1f62497.jpg_480x480.jpg_.webp",
      },
      {
        name: "Blanket",
        oldPrice: "$32.92",
        discountedPrice: "$7.99",
        rating: 4.5,
        image: "https://ae-pic-a1.aliexpress-media.com/kf/S414500b07cbc49538592f56fac15e0eez.jpg_480x480.jpg_.webp",
      },
      {
        name: "Wool Rug",
        oldPrice: "$6.54",
        discountedPrice: "$0.33",
        rating: 4.4,
        image: "https://ae-pic-a1.aliexpress-media.com/kf/S5e4cf7c4c77f44a6a4f320fbe13ae6171.jpg_480x480.jpg_.webp",
      },
      {
        name: "Golf T-shirt",
        oldPrice: "$5.09",
        discountedPrice: "$0.33",
        rating: 4.7,
        image: "https://ae-pic-a1.aliexpress-media.com/kf/S744ab00f2b3b4b5fa404af1ea087dcf2H.jpg_480x480.jpg_.webp",
      },
      {
        name: "Colored Pens",
        oldPrice: "$15.99",
        discountedPrice: "$5.50",
        rating: 4.6,
        image: "https://ae-pic-a1.aliexpress-media.com/kf/S6ad1b3187ce44e4a89c3cf752c4ce933j.jpg_480x480.jpg_.webp",
      },
      {
        name: "Robot Cleaner",
        oldPrice: "$50.50",
        discountedPrice: "$23.99",
        rating: 4.3,
        image: "https://ae-pic-a1.aliexpress-media.com/kf/S4c5194550d274c38894460bb7d6ae384v.jpg_480x480.jpg_.webp",
      },
      {
        name: "Toy",
        oldPrice: "$10.99",
        discountedPrice: "$3.99",
        rating: 4.5,
        image: "https://ae-pic-a1.aliexpress-media.com/kf/S9218cb0aa32b427491e40dd7ec05884au.jpg_480x480.jpg_.webp",
      },
      {
        name: "T-shirt",
        oldPrice: "$14.50",
        discountedPrice: "$6.50",
        rating: 4.8,
        image: "https://ae-pic-a1.aliexpress-media.com/kf/S8e9047c28c8a4e198199ed08580fd257z.jpg_480x480.jpg_.webp",
      },
    ]);

    const currentIndex = ref(0);
    const itemsPerPage = 4;
    const totalPages = Math.ceil(items.value.length / itemsPerPage);

    const nextSlide = () => {
      currentIndex.value = (currentIndex.value + 1) % totalPages;
    };

    const prevSlide = () => {
      currentIndex.value = (currentIndex.value - 1 + totalPages) % totalPages;
    };

    const handleProductClick = (item: { name: string }) => {
      alert(`Ürüne tıklandı: ${item.name}`);
    };

    return {
      items,
      currentIndex,
      nextSlide,
      prevSlide,
      handleProductClick,
    };
  },
});
</script>
