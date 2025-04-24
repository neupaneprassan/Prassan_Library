<template>
  <div class="p-6 max-w-4xl mx-auto space-y-6">
    <!-- Tabs -->
    <div class="flex space-x-4">
      <button
        class="px-4 py-2 bg-blue-600 text-white font-semibold rounded shadow"
      >
        Unread
      </button>
      <button class="px-4 py-2 bg-gray-200 text-gray-500 font-semibold rounded">
        Reading
      </button>
    </div>

    <!-- Today -->
    <div>
      <h2 class="text-blue-800 font-semibold mt-6 mb-4">Today</h2>
      <div
        v-for="n in 2"
        :key="'today-' + n"
        class="flex justify-between items-start bg-white rounded-xl p-4 shadow-sm border mb-4"
      >
        <div class="flex space-x-2">
          <span class="mt-1 w-2 h-2 bg-blue-500 rounded-full"></span>
          <div>
            <p class="font-medium text-blue-600">Kevin</p>
            <p class="text-sm text-gray-600 mt-1 leading-snug">
              ommodo facilisi accumsan gravida nisi consequat torquent. Nullam
              porttitor conubia interdum ullamcorper...
            </p>
          </div>
        </div>
        <div class="text-sm text-blue-600">18:20</div>
      </div>
    </div>

    <!-- Last months -->
    <div>
      <h2 class="text-blue-800 font-semibold mt-6 mb-4">Last months</h2>
      <div
        v-for="n in 3"
        :key="'last-' + n"
        class="flex justify-between items-start bg-white rounded-xl p-4 shadow-sm border mb-4 opacity-60"
      >
        <div class="flex space-x-2">
          <span class="mt-1 w-2 h-2 bg-gray-200 rounded-full"></span>
          <div>
            <p class="font-medium text-gray-600">Kevin</p>
            <p class="text-sm text-gray-600 mt-1 leading-snug">
              ommodo facilisi accumsan gravida nisi consequat torquent. Nullam
              porttitor conubia interdum ullamcorper...
            </p>
          </div>
        </div>
        <div class="text-sm text-blue-600">18:20</div>
      </div>
    </div>
  </div>
</template>
