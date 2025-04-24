<template>
  <div class="min-h-screen grid grid-cols-1 md:grid-cols-2">
    <!-- Left Section -->
    <div class="flex flex-col justify-center items-center bg-white p-6">
      <h1 class="text-3xl font-bold text-red-600 mb-2">Welcome</h1>
      <p class="text-sm text-gray-600 mb-6">
        Enter your email to sign up for this app
      </p>

      <div class="space-y-4 w-full max-w-xs">
        <button
          class="w-full bg-black text-white py-2 rounded-full hover:bg-gray-900"
        >
          Login in
        </button>
        <button
          class="w-full bg-black text-white py-2 rounded-full hover:bg-gray-900"
        >
          Sign up
        </button>
      </div>

      <div class="mt-6 text-sm text-blue-600 space-x-4">
        <a href="#">Engels</a>
        <a href="#">Dutch</a>
        <a href="#">French</a>
      </div>
    </div>

    <!-- Right Section -->
    <div class="hidden md:block relative">
      <img
        src="/images/5.jpg"
        alt="The Lies of the Artists"
        class="w-full h-full object-cover"
      />
      <div class="absolute bottom-10 left-10 text-white space-y-2 max-w-xs">
        <h2 class="text-4xl font-bold leading-tight">
          The Lies of the Artists
        </h2>
        <p class="text-md">Essays on Italian Art, 1450–1750</p>
        <p class="text-sm font-medium">Ingrid D. Rowland</p>
      </div>
    </div>
  </div>
</template>
