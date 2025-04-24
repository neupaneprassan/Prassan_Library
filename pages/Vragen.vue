<template>
  <div class="min-h-screen grid grid-cols-1 md:grid-cols-2">
    <!-- Left: Image -->
    <div class="hidden md:block">
      <img src="/images/11.jpg" class="w-full h-full object-cover" />
    </div>

    <!-- Right: Form Section -->
    <div class="bg-white p-10 flex flex-col justify-start">
      <h2 class="text-2xl font-bold text-red-600 mb-1">Additional questions</h2>
      <p class="text-sm text-gray-700 mb-8 max-w-md">
        We need a few more details to verify that you're a student or educator
        in an eligible
      </p>

      <form class="space-y-6 w-full max-w-md">
        <!-- Role -->
        <div>
          <label class="text-sm font-semibold text-blue-700">General?</label>
          <div class="flex gap-4 mt-1">
            <button
              type="button"
              class="text-sm px-3 py-1 rounded-full border border-blue-500 text-blue-700 hover:bg-blue-100"
            >
              Student
            </button>
            <button
              type="button"
              class="text-sm px-3 py-1 rounded-full border border-blue-500 text-blue-700 hover:bg-blue-100"
            >
              Teacher
            </button>
          </div>
        </div>

        <!-- Code -->
        <div>
          <label class="text-sm font-semibold text-blue-700"
            >Code from the student or teacher card?</label
          >
          <input
            type="text"
            placeholder="Code enter"
            class="w-full mt-1 border border-gray-300 rounded-md px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>

        <!-- Library visits -->
        <div>
          <label class="text-sm font-semibold text-blue-700"
            >How often do you visit the library on average per week?</label
          >
          <div class="flex gap-3 mt-1 text-sm text-gray-700">
            <span
              v-for="n in 7"
              :key="n"
              class="cursor-pointer hover:text-blue-700"
              >{{ n }}</span
            >
          </div>
        </div>

        <!-- Book type -->
        <div>
          <label class="text-sm font-semibold text-blue-700"
            >What kind of books do you like to read?</label
          >
          <textarea
            placeholder="I like to read books..."
            rows="3"
            class="w-full mt-1 border border-gray-300 rounded-md px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>

        <!-- Language -->
        <div>
          <label class="text-sm font-semibold text-blue-700"
            >Welke taal lees je om te boeken mogelijk? <br /><span
              class="text-xs font-normal"
              >Mogelijk meer optie</span
            ></label
          >
          <div class="flex gap-4 mt-2">
            <button
              type="button"
              class="text-sm px-3 py-1 rounded-full border border-gray-300 hover:bg-gray-100"
            >
              Dutch
            </button>
            <button
              type="button"
              class="text-sm px-3 py-1 rounded-full border border-gray-300 hover:bg-gray-100"
            >
              Engels
            </button>
            <button
              type="button"
              class="text-sm px-3 py-1 rounded-full border border-gray-300 hover:bg-gray-100"
            >
              French
            </button>
          </div>
        </div>

        <!-- Theme color -->
        <div>
          <label class="text-sm font-semibold text-blue-700"
            >Welke wil kleur toepassing deze website voor jou?</label
          >
          <div class="flex gap-6 mt-2">
            <div>
              <p class="text-sm mb-1">Default</p>
              <div class="flex gap-2">
                <div class="w-6 h-6 rounded bg-blue-500"></div>
                <div class="w-6 h-6 rounded bg-blue-900"></div>
              </div>
            </div>
            <div>
              <p class="text-sm mb-1">Other</p>
              <div class="flex gap-2">
                <div class="w-6 h-6 rounded bg-pink-400"></div>
                <div class="w-6 h-6 rounded bg-green-400"></div>
              </div>
            </div>
          </div>
        </div>
      </form>

      <!-- Save button -->
      <div class="mt-10">
        <button class="text-blue-700 font-semibold hover:underline">
          Save
        </button>
      </div>
    </div>
  </div>
</template>
