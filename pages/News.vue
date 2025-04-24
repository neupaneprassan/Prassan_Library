<template>
  <div class="px-6 md:px-16 py-12 space-y-12">
    <!-- Titel -->
    <h1 class="text-5xl font-bold text-blue-900">News</h1>

    <!-- Grote nieuwsblok -->
    <div class="space-y-4">
      <img
        src="/images/14.jpg"
        alt="Artwork"
        class="w-full object-cover rounded-xl shadow-md"
      />
      <div>
        <h2 class="text-2xl font-semibold text-blue-900">
          Potrait of the artist
        </h2>
        <p class="text-gray-600 text-sm mb-2">
          (<span class="text-blue-700">Xander Vertongen</span>)
        </p>
        <p class="text-sm text-gray-500 mb-2">04.03.2025</p>
        <p class="text-gray-500 text-sm leading-relaxed line-clamp-4">
          Nullam porttitorconubia interdum ullamcorper, facilisi curabitur
          pellentesque...
        </p>
      </div>
    </div>

    <!-- Carousel / kleine previews -->
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
      <div
        v-for="i in 3"
        :key="i"
        class="bg-white shadow rounded-lg overflow-hidden"
      >
        <img
          src="/images/17.jpg"
          alt="Thumbnail"
          class="h-36 w-full object-cover"
        />
        <div class="p-4">
          <h3 class="text-blue-900 font-medium text-sm">
            Potrait of the artist
          </h3>
          <p class="text-xs text-gray-500 mb-2">
            interdum ullamcorper, facilisi curabitur pellentesque...
          </p>
          <button
            class="text-white bg-blue-700 text-xs px-3 py-1 rounded hover:bg-blue-800"
          >
            Read more
          </button>
        </div>
      </div>
    </div>

    <!-- Carousel dots (optioneel) -->
    <div class="flex justify-center items-center gap-2 mt-6">
      <span
        v-for="dot in 7"
        :key="dot"
        class="h-2 w-2 rounded-full bg-gray-400"
      ></span>
      <span class="h-2 w-2 rounded-full bg-blue-500"></span>
    </div>
  </div>
</template>

<style>
.px-6 {
  padding-left: 300px;
  padding-right: 300px;
}
</style>
