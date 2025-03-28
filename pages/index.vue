<template>
  <div>
    <h2 class="text-2xl font-bold text-blue-800">Homepage</h2>

    <div class="mt-4"></div>

    <h3 class="text-xl font-semibold text-blue-600 mt-6">
      Special collections
    </h3>
    <div class="wrapper">
      <img src="" alt="" />
      <div class=""></div>
    </div>

    <div class="grid grid-cols-2 gap-4 mt-4">
      <Card v-for="item in 4" :key="item" />
    </div>
  </div>
</template>
