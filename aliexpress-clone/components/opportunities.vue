<template>
  <div class="max-w-screen-lg mx-auto p-4">
    <div class="text-center mb-4">
      <h2 class="text-2xl font-semibold">Süper Fırsatlar</h2>
      <div class="flex justify-center items-center text-red-600 mt-2">
        <img
          height="24"
          width="24"
          src="https://ae01.alicdn.com/kf/S1fa2ebed8eb04c4597523704c386ff5ag/48x48.gif"
          class="cards--dynamicImg--3M667J1"
          data-spm-anchor-id="a2g0o.home.superdeal.i9.4c5f10d0KjStDr"
        />
        Bitiş: {{ countdown }}
      </div>
    </div>

    <div class="relative">
      <button
        @click="prevSlide"
        class="absolute left-0 top-1/2 transform -translate-y-1/2 z-10 bg-white p-2 rounded-full shadow-lg hover:bg-gray-100"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="w-6 h-6 text-gray-600"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M15 19l-7-7 7-7"
          />
        </svg>
      </button>

      <div class="flex overflow-hidden">
        <div
          v-for="(product, index) in visibleProducts"
          :key="index"
          class="w-1/3 px-2 transition-transform duration-300"
        >
          <div
            class="border p-4 rounded-lg shadow-lg transform hover:scale-105 transition-transform duration-300"
          >
            <img
              :src="product.image"
              :alt="product.name"
              class="w-full h-40 object-cover rounded"
            />
            <h3 class="mt-2 text-sm text-gray-700 truncate">
              {{ product.name }}
            </h3>
            <div class="mt-1 flex items-center justify-between">
              <span class="text-red-600 font-semibold"
                >{{ product.price }}TL</span
              >
              <span class="text-gray-500 line-through text-sm"
                >{{ product.oldPrice }}TL</span
              >
            </div>
            <span
              class="text-white text-xs bg-red-500 px-2 py-1 rounded mt-2 inline-block"
            >
              -{{ product.discount }}%
            </span>
          </div>
        </div>
      </div>

      <button
        @click="nextSlide"
        class="absolute right-0 top-1/2 transform -translate-y-1/2 z-10 bg-white p-2 rounded-full shadow-lg hover:bg-gray-100"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="w-6 h-6 text-gray-600"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M9 5l7 7-7 7"
          />
        </svg>
      </button>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref, computed, onMounted, onUnmounted } from "vue";

interface Product {
  name: string;
  price: number;
  oldPrice: number;
  discount: number;
  image: string;
}

export default defineComponent({
  name: "ProductSlider",
  setup() {
    const products = ref<Product[]>([
      {
        name: "Moda 8mm kırmızı oluk eğimli kenar...",
        price: 26.88,
        oldPrice: 75.11,
        discount: 64,
        image:
          "https://ae-pic-a1.aliexpress-media.com/kf/Sf705fb04bb3043389c00ea8eeb9a5551h.png_480x480.png_.webp",
      },
      {
        name: "Flipo Flip alaşım kare altıgen dönen...",
        price: 36.45,
        oldPrice: 62.87,
        discount: 42,
        image:
          "https://ae-pic-a1.aliexpress-media.com/kf/H98df8c631b64474e9e560b957375d1f4c.jpg_480x480.jpg_.webp",
      },
      {
        name: "Lüks darbe mat telefon kılıfı için...",
        price: 38.29,
        oldPrice: 56.33,
        discount: 32,
        image:
          "https://ae-pic-a1.aliexpress-media.com/kf/S6a75e5ebd38045b4a32d245d30e01df6e.jpg_480x480.jpg_.webp",
      },
      {
        name: "Yeni model akıllı saat ekran koruyucu...",
        price: 45.29,
        oldPrice: 78.99,
        discount: 43,
        image:
          "https://ae-pic-a1.aliexpress-media.com/kf/S6d11be9c50b148f2928e924a3dd958a9N.jpg_480x480.jpg_.webp",
      },
      {
        name: "Yeni model akıllı saat ekran koruyucu...",
        price: 45.29,
        oldPrice: 78.99,
        discount: 43,
        image:
          "https://ae-pic-a1.aliexpress-media.com/kf/Se8a368aa85434fcb80be6d3b282f3876X.png_480x480.png_.webp",
      },
      {
        name: "Yeni model akıllı saat ekran koruyucu...",
        price: 45.29,
        oldPrice: 78.99,
        discount: 43,
        image:
          "https://ae-pic-a1.aliexpress-media.com/kf/Sfb17027661ad47ed9b60927d62c614a46.jpg_480x480.jpg_.webp",
      },
    ]);

    const currentIndex = ref(0);

    const endTime = new Date().getTime() + 24 * 60 * 60 * 1000;
    const countdown = ref("");

    const updateCountdown = () => {
      const now = new Date().getTime();
      const remainingTime = endTime - now;

      if (remainingTime <= 0) {
        countdown.value = "00:00:00";
        clearInterval(timer);
        return;
      }

      const hours = String(
        Math.floor((remainingTime / (1000 * 60 * 60)) % 24)
      ).padStart(2, "0");
      const minutes = String(
        Math.floor((remainingTime / (1000 * 60)) % 60)
      ).padStart(2, "0");
      const seconds = String(Math.floor((remainingTime / 1000) % 60)).padStart(
        2,
        "0"
      );

      countdown.value = `${hours}:${minutes}:${seconds}`;
    };

    let timer: ReturnType<typeof setInterval>;
    onMounted(() => {
      updateCountdown();
      timer = setInterval(updateCountdown, 1000);
    });

    onUnmounted(() => {
      clearInterval(timer);
    });

    const visibleProducts = computed(() =>
      products.value.slice(currentIndex.value, currentIndex.value + 3)
    );

    const nextSlide = () => {
      if (currentIndex.value + 3 < products.value.length) {
        currentIndex.value++;
      }
    };

    const prevSlide = () => {
      if (currentIndex.value > 0) {
        currentIndex.value--;
      }
    };

    return {
      products,
      currentIndex,
      visibleProducts,
      nextSlide,
      prevSlide,
      countdown,
    };
  },
});
</script>
