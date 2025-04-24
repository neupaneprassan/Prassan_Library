<template>
  <div class="px-16 py-10 min-h-screen">
    <h1 class="text-3xl font-bold mb-10">Favoriet</h1>

    <div class="space-y-10">
      <!-- Card item -->
      <div
        v-for="index in 6"
        :key="index"
        class="flex justify-between border-b pb-10"
      >
        <!-- Links: Afbeelding -->
        <div class="flex-shrink-0">
          <img
            src="/images/5.jpg"
            alt="Book cover"
            class="w-32 h-32 object-cover rounded-md"
          />
        </div>

        <!-- Midden: Titel + tekst -->
        <div class="flex-1 px-8">
          <h2 class="text-blue-700 font-semibold text-lg">
            Portrait of the artist
          </h2>
          <p class="text-gray-500 text-sm mb-1">Artist</p>
          <p class="text-gray-600 text-sm mb-4">
            Ula volutpat turpis nam etiam egestas morbi feu... suspendisse donec
            lacus
          </p>

          <div class="flex space-x-12 text-sm text-gray-600">
            <div>
              <p class="font-bold text-black">200</p>
              <p class="text-gray-400">Page</p>
            </div>
            <div>
              <p class="font-bold text-black">Engels</p>
              <p class="text-gray-400">Language</p>
            </div>
            <div>
              <p class="font-bold text-black">2019</p>
              <p class="text-gray-400">Release</p>
            </div>
          </div>
        </div>

        <!-- Rechts: Read more + Hart -->
        <div class="Box-fav flex-direction items-end justify-between space-y-4">
          <button
            class="bg-[#3952d0] text-white text-sm px-5 py-1.5 rounded-full hover:bg-blue-700 shadow-sm"
          >
            Read more
          </button>

          <button>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6 text-[#3952d0]"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              stroke-width="2"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M12 21.35l-1.45-1.32C5.4 15.36 
                2 12.28 2 8.5 2 6.5 3.5 5 5.5 5 
                c1.54 0 3.04.99 3.57 2.36h1.87C13.46 
                5.99 14.96 5 16.5 5 18.5 5 20 6.5 
                20 8.5c0 3.78-3.4 6.86-8.55 
                11.54L12 21.35z"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// voorlopig geen logica
</script>

<style>
.py-10 {
  padding-left: 300px;
  padding-right: 300px;
}
.Box-fav {
  display: flex;
  gap: 10px;
}
.border-b {
  border-bottom-width: 3px;
}
</style>
