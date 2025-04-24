<template>
  <div class="min-h-screen grid grid-cols-1 md:grid-cols-2">
    <!-- Left: Sign Up Form -->
    <div class="flex flex-col justify-center items-center bg-white px-6 py-8">
      <h1 class="text-3xl font-bold text-red-600 mb-1">Sign up</h1>
      <p class="text-sm text-gray-600 mb-6">
        Enter your email to sign up for this app
      </p>

      <form class="w-full max-w-xs space-y-4">
        <div>
          <label class="text-sm text-blue-700 font-medium">Forname</label>
          <input
            type="text"
            placeholder="enter forname"
            class="w-full border border-gray-300 rounded-md px-4 py-2 mt-1 focus:outline-none focus:ring-2 focus:ring-black"
          />
        </div>

        <div>
          <label class="text-sm text-blue-700 font-medium">Last name</label>
          <input
            type="text"
            placeholder="enter last name"
            class="w-full border border-gray-300 rounded-md px-4 py-2 mt-1 focus:outline-none focus:ring-2 focus:ring-black"
          />
        </div>

        <div>
          <label class="text-sm text-blue-700 font-medium">Email</label>
          <input
            type="email"
            placeholder="email@domain.com"
            class="w-full border border-gray-300 rounded-md px-4 py-2 mt-1 focus:outline-none focus:ring-2 focus:ring-black"
          />
        </div>

        <div>
          <label class="text-sm text-blue-700 font-medium">Password</label>
          <div class="relative">
            <input
              type="password"
              placeholder="enter password"
              class="w-full border border-gray-300 rounded-md px-4 py-2 mt-1 focus:outline-none focus:ring-2 focus:ring-black"
            />
            <span class="absolute right-3 top-3 text-gray-400 cursor-pointer">
            </span>
          </div>
        </div>

        <button
          type="submit"
          class="w-full bg-black text-white py-2 rounded-full hover:bg-gray-900"
        >
          Continue
        </button>
      </form>

      <!-- Divider -->
      <div class="my-4 text-gray-400 w-full max-w-xs flex items-center">
        <hr class="flex-grow border-t border-gray-300" />
        <span class="mx-2 text-sm">or</span>
        <hr class="flex-grow border-t border-gray-300" />
      </div>

      <button
        class="w-full max-w-xs bg-black text-white py-2 rounded-full hover:bg-gray-900"
      >
        Sign up
      </button>

      <p class="text-sm text-gray-500 mt-4">Sign up with</p>

      <!-- Social Icons (placeholders) -->
      <div class="flex gap-4 mt-2">
        <span>📘</span>
        <span>🔵</span>
        <span>🟥</span>
        <span>🍎</span>
      </div>

      <p class="text-xs text-gray-400 mt-4 text-center max-w-xs">
        By clicking continue, you agree to our
        <span class="underline cursor-pointer">Terms of Service</span> and
        <span class="underline cursor-pointer">Privacy Policy</span>
      </p>

      <p class="text-sm mt-4 text-gray-700">
        Already have an account?
        <span class="underline cursor-pointer text-black font-medium"
          >Log in</span
        >
      </p>
    </div>

    <!-- Right: Image -->
    <div class="hidden md:block relative">
      <img
        src="/images/12.jpg"
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
