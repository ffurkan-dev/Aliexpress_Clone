<template>
  <div
    class="flex flex-col md:flex-row bg-white p-4 rounded-lg shadow-md w-full max-w-5xl mx-auto"
  >
    
    <div class="w-full md:w-1/2 mb-4 md:mb-0">
      <img :src="selectedImage" alt="Ürün Görseli" class="rounded-md" />
    </div>

    
    <div class="w-full md:w-1/2 md:pl-6 flex flex-col">
      
      <div
        class="bg-pink-500 text-white text-sm font-semibold px-4 py-2 rounded-md mb-4"
      >
        ⚡ 479,82 TL tasarruf edin
      </div>

      
      <div class="mb-4">
        <p class="text-3xl font-bold text-gray-800">124,31 TL</p>
        <div class="flex items-center space-x-2">
          <span class="text-sm text-gray-500 line-through">604,13 TL</span>
          <span class="text-sm text-red-500 font-semibold">79% indirim</span>
        </div>
        <p class="text-xs text-gray-500">
          Vergiden önce gösterilen fiyat | Ekstra %1 İndirim
        </p>
      </div>

      
      <div class="mb-4">
        <h2 class="text-gray-800 text-base font-semibold">
          Evrensel Cep Telefonu Standı Ayarlanabilir Tembel Standı Dönebilen
          Başucu Standı Masaüstü Canlı Akış Selfie'ler Telefon Aksesuarları
        </h2>
      </div>

      
      <div class="flex items-center mb-4 space-x-1">
        <span class="flex">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="currentColor"
            class="size-6"
          >
            <path
              fill-rule="evenodd"
              d="M10.788 3.21c.448-1.077 1.976-1.077 2.424 0l2.082 5.006 5.404.434c1.164.093 1.636 1.545.749 2.305l-4.117 3.527 1.257 5.273c.271 1.136-.964 2.033-1.96 1.425L12 18.354 7.373 21.18c-.996.608-2.231-.29-1.96-1.425l1.257-5.273-4.117-3.527c-.887-.76-.415-2.212.749-2.305l5.404-.434 2.082-5.005Z"
              clip-rule="evenodd"
            />
          </svg>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="currentColor"
            class="size-6"
          >
            <path
              fill-rule="evenodd"
              d="M10.788 3.21c.448-1.077 1.976-1.077 2.424 0l2.082 5.006 5.404.434c1.164.093 1.636 1.545.749 2.305l-4.117 3.527 1.257 5.273c.271 1.136-.964 2.033-1.96 1.425L12 18.354 7.373 21.18c-.996.608-2.231-.29-1.96-1.425l1.257-5.273-4.117-3.527c-.887-.76-.415-2.212.749-2.305l5.404-.434 2.082-5.005Z"
              clip-rule="evenodd"
            />
          </svg>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="currentColor"
            class="size-6"
          >
            <path
              fill-rule="evenodd"
              d="M10.788 3.21c.448-1.077 1.976-1.077 2.424 0l2.082 5.006 5.404.434c1.164.093 1.636 1.545.749 2.305l-4.117 3.527 1.257 5.273c.271 1.136-.964 2.033-1.96 1.425L12 18.354 7.373 21.18c-.996.608-2.231-.29-1.96-1.425l1.257-5.273-4.117-3.527c-.887-.76-.415-2.212.749-2.305l5.404-.434 2.082-5.005Z"
              clip-rule="evenodd"
            />
          </svg>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="currentColor"
            class="size-6"
          >
            <path
              fill-rule="evenodd"
              d="M10.788 3.21c.448-1.077 1.976-1.077 2.424 0l2.082 5.006 5.404.434c1.164.093 1.636 1.545.749 2.305l-4.117 3.527 1.257 5.273c.271 1.136-.964 2.033-1.96 1.425L12 18.354 7.373 21.18c-.996.608-2.231-.29-1.96-1.425l1.257-5.273-4.117-3.527c-.887-.76-.415-2.212.749-2.305l5.404-.434 2.082-5.005Z"
              clip-rule="evenodd"
            />
          </svg>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="currentColor"
            class="size-6"
          >
            <path
              fill-rule="evenodd"
              d="M10.788 3.21c.448-1.077 1.976-1.077 2.424 0l2.082 5.006 5.404.434c1.164.093 1.636 1.545.749 2.305l-4.117 3.527 1.257 5.273c.271 1.136-.964 2.033-1.96 1.425L12 18.354 7.373 21.18c-.996.608-2.231-.29-1.96-1.425l1.257-5.273-4.117-3.527c-.887-.76-.415-2.212.749-2.305l5.404-.434 2.082-5.005Z"
              clip-rule="evenodd"
            />
          </svg>
        </span>
        <span class="text-sm text-gray-700">5.0</span>
        <span class="text-sm text-gray-500">(1400 Yorum)</span>
        <span class="text-sm text-gray-500 ml-2">5000+ satıldı</span>
      </div>

      
      <div class="mb-4">
        <p class="text-gray-700 text-sm font-semibold mb-2">Renk: White</p>
        <div class="flex space-x-2">
          <img
            v-for="(image, index) in colorOptions"
            :key="index"
            :src="image"
            alt="Renk Seçimi"
            class="w-12 h-12 border rounded-md cursor-pointer"
            @click="updateSelectedImage(image)"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "ProductCard",
  setup() {
    
    const selectedImage = ref<string>(
      "https://ae-pic-a1.aliexpress-media.com/kf/Sf705fb04bb3043389c00ea8eeb9a5551h/Evrensel-Cep-Telefonu-Stand-Ayarlanabilir-Tembel-Stand-D-nebilen-Ba-ucu-Stand-Masa-st-Canl-Ak.png_.webp"
    );

    
    const colorOptions = ref<string[]>([
      "https://ae-pic-a1.aliexpress-media.com/kf/S82d76c92c93b4dcf812b6b33dca57f20e.jpg_120x120.jpg_.webp",
      "https://ae-pic-a1.aliexpress-media.com/kf/Sc513b07cb22a467181d3a57f86dfa71dj.jpg_120x120.jpg_.webp",
      "https://ae-pic-a1.aliexpress-media.com/kf/Sf705fb04bb3043389c00ea8eeb9a5551h/Evrensel-Cep-Telefonu-Stand-Ayarlanabilir-Tembel-Stand-D-nebilen-Ba-ucu-Stand-Masa-st-Canl-Ak.png_.webp",
    ]);

    
    const updateSelectedImage = (image: string): void => {
      selectedImage.value = image;
    };

    return {
      selectedImage,
      colorOptions,
      updateSelectedImage,
    };
  },
});
</script>
