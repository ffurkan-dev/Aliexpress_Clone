<template>
  <header class="bg-black text-white">
    <div class="bg-black">
      <div class="container mx-auto flex items-center justify-center py-3 px-6">
        <div
          class="flex items-center justify-center space-x-6 w-full max-w-4xl"
        >
          <div class="flex items-center space-x-2">
            <img src="/logo.png" alt="Logo" class="h-8" />
          </div>

          <div class="flex-grow max-w-xl">
            <div class="relative">
              <input
                type="text"
                placeholder="Search for items"
                class="w-full py-2 px-4 text-black rounded-lg"
              />
              <button
                class="absolute right-2 top-1/2 -translate-y-1/2 bg-red-500 text-white px-4 py-1 rounded-2xl"
              >
                <svg
                  fill="#000000"
                  height="24px"
                  width="24px"
                  version="1.1"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 512 512"
                  xmlns:xlink="http://www.w3.org/1999/xlink"
                  enable-background="new 0 0 512 512"
                  stroke="#000000"
                  stroke-width="0.00512"
                >
                  <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                  <g
                    id="SVGRepo_tracerCarrier"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  ></g>
                  <g id="SVGRepo_iconCarrier">
                    <g>
                      <path
                        d="m495,466.1l-119.2-119.2c29.1-35.5 46.5-80.8 46.5-130.3 0-113.5-92.1-205.6-205.6-205.6-113.6,0-205.7,92.1-205.7,205.7s92.1,205.7 205.7,205.7c49.4,0 94.8-17.4 130.3-46.5l119.1,119.1c8,8 20.9,8 28.9,0 8-8 8-20.9 0-28.9zm-443.2-249.4c-1.42109e-14-91 73.8-164.8 164.8-164.8 91,0 164.8,73.8 164.8,164.8s-73.8,164.8-164.8,164.8c-91,0-164.8-73.8-164.8-164.8z"
                      ></path>
                    </g>
                  </g>
                </svg>
              </button>
            </div>
          </div>


          <div class="flex items-center space-x-4">
            <div class="relative">
              <button class="text-sm flex items-center">
                <span class="mr-1">EN/USD</span>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-4 w-4"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M19 9l-7 7-7-7"
                  />
                </svg>
              </button>
            </div>

            <button class="text-sm">Sign in / Register</button>
            <a href="#" class="relative">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-6 w-6"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M3 3h18M9 9h6m-9 3h12M9 15h6"
                />
              </svg>
              <span
                class="absolute top-0 right-0 bg-red-500 text-xs text-white rounded-full px-1"
                >2</span
              >
            </a>
          </div>
        </div>
      </div>
    </div>

    <div class="bg-black">
      <div
        class="container mx-auto flex items-center justify-center py-3 px-6 space-x-6"
      >

        <div class="relative group">
          <button
            class="bg-gray-700 px-4 py-2 rounded-full text-sm flex items-center hover:bg-gray-600"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4 mr-2"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
            All Categories
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4 ml-2"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M19 9l-7 7-7-7"
              />
            </svg>
          </button>
          <div
            class="absolute left-0 mt-2 bg-white text-black py-2 w-48 rounded shadow-lg hidden group-hover:block"
          >
            <a href="#" class="block px-4 py-2 hover:bg-gray-200"
              >Electronics</a
            >
            <a href="#" class="block px-4 py-2 hover:bg-gray-200">Fashion</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-200"
              >Home & Garden</a
            >
            <a href="#" class="block px-4 py-2 hover:bg-gray-200">Toys</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-200">Sports</a>
          </div>
        </div>

        <a
          href="#"
          class="text-sm bg-black px-3 py-1 rounded-full text-red-500"
        >
          3 from $0.99
        </a>
        <a
          href="#"
          class="text-sm px-3 py-2 hover:bg-gray-600 hover:rounded-full"
          >Welcome Deal</a
        >
        <a
          href="#"
          class="text-sm px-3 py-2 hover:bg-gray-600 hover:rounded-full"
          >Ship from US</a
        >
        <a
          href="#"
          class="text-sm px-3 py-2 hover:bg-gray-600 hover:rounded-full"
          >Wigs</a
        >
        <a
          href="#"
          class="text-sm px-3 py-2 hover:bg-gray-600 hover:rounded-full"
          >SuperDeals</a
        >
        <a
          href="#"
          class="text-sm px-3 py-2 hover:bg-gray-600 hover:rounded-full"
          >AIExpress Business</a
        >

        <div class="relative">
          <button
            class="text-sm px-3 py-2 hover:bg-gray-600 hover:rounded-full flex items-center"
          >
            More
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4 ml-1"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M19 9l-7 7-7-7"
              />
            </svg>
          </button>
          <div
            class="absolute left-0 mt-2 bg-gray-800 text-white py-2 w-40 rounded shadow-lg hidden group-hover:block"
          >
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Option 1</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Option 2</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Option 3</a>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
.relative:hover .hidden {
  display: block;
}
</style>
