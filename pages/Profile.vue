<template>
  <div class="p-6 space-y-10">
    <!-- Tabs -->
    <div class="flex space-x-8 text-lg font-semibold border-b border-gray-200">
      <NuxtLink to="/profile" class="pb-2">My Profile</NuxtLink>
      <NuxtLink
        to="/dashboard"
        class="pb-2 border-b-2 border-blue-600 text-blue-600"
        >Dashboard</NuxtLink
      >
      <NuxtLink to="/settings" class="pb-2">Settings</NuxtLink>
    </div>

    <!-- Je Activiteit -->
    <div>
      <h2 class="text-xl font-bold mb-4 text-gray-800">Je activiteit</h2>
      <div class="flex space-x-10 text-center">
        <div>
          <iconify-icon
            icon="mdi:heart"
            class="text-blue-600 text-2xl"
          ></iconify-icon>
          <div class="font-bold">12</div>
          <div class="text-sm text-gray-600">Likes</div>
        </div>
        <div>
          <iconify-icon
            icon="mdi:clipboard-text"
            class="text-blue-600 text-2xl"
          ></iconify-icon>
          <div class="font-bold">6</div>
          <div class="text-sm text-gray-600">Book listed</div>
        </div>
        <div>
          <iconify-icon
            icon="mdi:comment-text"
            class="text-blue-600 text-2xl"
          ></iconify-icon>
          <div class="font-bold">32</div>
          <div class="text-sm text-gray-600">Opmerking</div>
        </div>
      </div>
    </div>

    <!-- Lenen book -->
    <div>
      <h2 class="text-xl font-bold text-gray-800 mb-4">Lenen book</h2>
      <div class="space-y-4">
        <div>
          <div class="text-sm font-semibold text-blue-800">Uitgeleend (5)</div>
          <div class="w-full h-2 bg-gray-200 rounded">
            <div
              class="h-2 bg-gray-400 rounded transition-all duration-500"
              style="width: 40%"
            ></div>
          </div>
        </div>
        <div>
          <div class="text-sm font-semibold text-blue-800">Reserveer (8)</div>
          <div class="w-full h-2 bg-gray-200 rounded">
            <div
              class="h-2 bg-blue-600 rounded transition-all duration-500"
              :style="{ width: reservedPercent + '%' }"
            ></div>
          </div>
        </div>
      </div>
    </div>

    <!-- Own book -->

    <h2 class="text-xl font-bold mb-4 text-gray-800">Eigen boek</h2>
    <div class="flex gap-4 p-4 border-b border-gray-300">
      <img
        src="/images/5.jpg"
        alt="Boek cover"
        class="w-32 h-32 object-cover rounded-md"
      />
      <div class="flex-1">
        <h2 class="text-xl font-bold text-blue-700">Potrait of the artist</h2>
        <p class="text-gray-600 font-semibold">(Xander Vertongen)</p>
        <div class="mt-2 text-gray-700 font-semibold">
          Publiek <span class="ml-2 font-normal">20.03.2025</span>
        </div>
      </div>
      <div class="flex gap-6 items-center">
        <div class="flex flex-col items-center text-blue-700">
          <span class="font-bold">Likes</span>
          <div class="flex items-center gap-1">
            <Icon name="mdi:heart" class="text-blue-700" />
            <span>12</span>
          </div>
        </div>
        <div class="flex flex-col items-center text-blue-700">
          <span class="font-bold">Geleend</span>
          <div class="flex items-center gap-1">
            <Icon name="mdi:format-list-bulleted" class="text-blue-700" />
            <span>6</span>
          </div>
        </div>
        <div class="flex flex-col items-center text-blue-700">
          <span class="font-bold">Opmerking</span>
          <div class="flex items-center gap-1">
            <Icon name="mdi:comment" class="text-blue-700" />
            <span>32</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const reservedPercent = ref(70);
const showBooks = ref(true);
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: all 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
.p-6 {
  padding-left: 300px;
  padding-right: 300px;
}
</style>
