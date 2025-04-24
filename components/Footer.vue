<template>
  <div class="footer mt-10">
    <hr class="mb-4" />

    <div
      class="flex flex-col md:flex-row justify-between items-center text-blue-700 px-4"
    >
      <!-- Adres en Email -->
      <div
        class="text-footer flex-col md:flex-row space-y-1 md:space-y-0 md:space-x-4 text-center md:text-left"
      >
        <span>Rue des Palais 70, 1030 Bruxelles</span>
        <a href="mailto:Sint-Lukas@gmail.com" class="hover:underline"
          >Sint-Lukas@gmail.com</a
        >
      </div>

      <!-- Privacy links -->
      <div class="text-footer space-x-4 mt-2 md:mt-0">
        <a href="#" class="hover:underline">Privacy policy</a>

        <NuxtLink to="/Cookies policy">Cookies policy</NuxtLink>
      </div>

      <!-- Social media -->
      <div class="flex space-x-3 mt-2 md:mt-0">
        <a href="#" class="hover:opacity-75">
          <svg class="w-5 h-5 fill-blue-700" viewBox="0 0 24 24">
            <path
              d="M22 12.07C22 6.49 17.52 2 12 2S2 6.49 2 12.07c0 4.85 3.44 8.87 7.94 9.8v-6.93H7.1v-2.87h2.84V9.41c0-2.8 1.66-4.35 4.21-4.35 1.22 0 2.5.22 2.5.22v2.75h-1.41c-1.39 0-1.82.87-1.82 1.76v2.11h3.09l-.49 2.87h-2.6V22c4.5-.93 7.94-4.95 7.94-9.8z"
            />
          </svg>
        </a>
        <a href="#" class="hover:opacity-75">
          <svg class="w-5 h-5 fill-blue-700" viewBox="0 0 24 24">
            <path
              d="M7.75 2h8.5A5.75 5.75 0 0 1 22 7.75v8.5A5.75 5.75 0 0 1 16.25 22h-8.5A5.75 5.75 0 0 1 2 16.25v-8.5A5.75 5.75 0 0 1 7.75 2zm0 1.5A4.25 4.25 0 0 0 3.5 7.75v8.5A4.25 4.25 0 0 0 7.75 20.5h8.5A4.25 4.25 0 0 0 20.5 16.25v-8.5A4.25 4.25 0 0 0 16.25 3.5h-8.5zm8.25 3.25a.75.75 0 1 1 0 1.5.75.75 0 0 1 0-1.5zM12 7a5 5 0 1 1 0 10 5 5 0 0 1 0-10z"
            />
          </svg>
        </a>
      </div>
    </div>

    <!-- ColorMode en GitHub link -->
    <div class="colormode-b justify-between items-center mt-6">
      <div class="colormode-b basis-11/12">
        <ColorMode />
      </div>
      <div class="flex-1 basis-1/12 text-right">
        <NuxtLink
          to="https://github.com/bureaupixel/Nuxt-collections"
          target="_blank"
          class="hover:opacity-75 inline-block"
        >
          <GithubIcon />
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<style>
.footer {
  margin: 50px 50px;
}
.text-footer {
  font-size: 12px;
}
</style>
