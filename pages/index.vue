<template>
  <div class="homepage max-w-7xl mx-auto">
    <!-- Pagina titel -->
    <h1 class="text-2xl font-bold text-blue-800">Homepage</h1>

    <!-- Hero Sectie -->
    <div class="flex flex-col lg:flex-row mt-6 gap-6">
      <img
        src="/images/5.jpg"
        alt="Hero Image"
        class="rounded shadow w-full lg:w-1/2"
      />
      <div>
        <h3 class="text-xl font-semibold text-blue-600">
          Portrait of the artist
        </h3>
        <p class="text-gray-600 mt-1">(Xander Vertongen)</p>
        <p class="mt-2 text-gray-700">
          Curabitur pellentesque posuere ex at posuere. Integer gravida sem
          sagittis lorem congue. Vivamus volutpat dictum sem, vitae fermentum
          risus.Curabitur pellentesque posuere ex at posuere. Integer gravida
          sem sagittis lorem congue. Vivamus volutpat dictum sem, vitae
          fermentum risus.
        </p>
        <!-- Dots + Arrow onder afbeelding -->
        <div class="flex items-center space-x-2 mt-3">
          <div id="dots" class="flex space-x-1"></div>

          <button @click="nextSlide" class="text-blue-600">
            <svg
              class="w-4 h-4"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              viewBox="0 0 24 24"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M9 5l7 7-7 7"
              />
            </svg>
          </button>
        </div>
        <button class="mt-4 px-4 py-2 bg-blue-700 text-white rounded">
          Read more
        </button>
      </div>
    </div>
    <div class="flex items-center space-x-2">
      <!-- Dots -->

      <!-- Arrow -->
      <button class="text-blue-600">
        <svg
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          viewBox="0 0 24 24"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M9 5l7 7-7 7"
          />
        </svg>
      </button>
    </div>
    <!-- Special collections -->
    <h3 class="text-xl font-semibold text-blue-600 mt-10">
      Special collections
    </h3>

    <div
      class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6 mt-4"
    >
      <div v-for="item in 4" :key="item" class="bg-white rounded shadow p-4">
        <img src="/images/11.jpg" alt="Art" class="rounded" />
        <h4 class="mt-3 font-semibold text-gray-800">Portrait of the artist</h4>
        <p class="text-sm text-gray-600 mt-1">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit.
        </p>
        <div class="flex justify-between items-center mt-4">
          <button class="text-sm text-white bg-blue-600 px-3 py-1 rounded">
            Read more
          </button>
          <button class="text-gray-500 hover:text-red-500 text-lg">♡</button>
        </div>
      </div>
    </div>
    <!-- Horizontale slider sectie -->
    <h3 class="text-xl font-semibold text-blue-600 mt-10">Popular</h3>
    <div class="overflow-x-auto whitespace-nowrap py-6">
      <div class="inline-flex gap-4">
        <div
          v-for="n in 6"
          :key="n"
          class="w-64 flex-shrink-0 bg-white rounded-lg shadow p-4"
        >
          <img
            :src="n === 1 ? '/images/5.jpg' : '/images/11.jpg'"
            alt="Portrait"
            class="rounded w-full h-40 object-cover"
          />
          <h4 class="mt-3 font-semibold text-blue-800 text-sm">
            Portrait of the artist
          </h4>
          <p class="text-xs text-gray-500 mb-1">Artist</p>
          <p class="text-sm text-gray-600 line-clamp-3">
            nam etiam egestas morbi feu... suspendisse donec locus nam etiam
            egestas morbi feu...
          </p>
          <div class="flex justify-between items-center mt-4">
            <button class="text-sm text-white bg-blue-600 px-3 py-1 rounded">
              Read more
            </button>
            <button class="text-gray-500 hover:text-blue-600 text-lg">♡</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// Geen script nodig als het enkel statisch is
</script>

<style>
/* Extra CSS kun je hier toevoegen indien nodig */
</style>

<span
  class="iconify"
  data-icon="material-symbols:account-circle-full"
  data-inline="false"
></span>
<span
  class="iconify"
  data-icon="material-symbols:account-circle-full"
  data-inline="false"
></span>

<style>
.homepage {
  margin: 25px 250px;
}
.text-2xl {
  margin-top: 80px;
  margin-bottom: 40px;
}
</style>
