<template>
  <div class="max-w-4xl mx-auto px-4 py-16 bg-white rounded-lg shadow-md">
    <h2 class="text-3xl font-bold text-blue-600 mb-10">Contact us</h2>
    <form class="space-y-6">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div>
          <label class="block text-sm font-semibold text-gray-700 mb-1"
            >First name</label
          >
          <input
            type="text"
            placeholder="First name enter"
            class="w-full border border-gray-300 rounded-md p-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>
        <div>
          <label class="block text-sm font-semibold text-gray-700 mb-1"
            >Last name</label
          >
          <input
            type="text"
            placeholder="Last name enter"
            class="w-full border border-gray-300 rounded-md p-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>
      </div>

      <div>
        <label class="block text-sm font-semibold text-gray-700 mb-1"
          >E-mail</label
        >
        <input
          type="email"
          placeholder="Email enter"
          class="w-full border border-gray-300 rounded-md p-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
        />
      </div>

      <div>
        <label class="block text-sm font-semibold text-gray-700 mb-1"
          >Phone number</label
        >
        <input
          type="tel"
          placeholder="Phone number enter"
          class="w-full border border-gray-300 rounded-md p-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
        />
      </div>

      <div>
        <label class="block text-sm font-semibold text-gray-700 mb-1"
          >Message</label
        >
        <textarea
          rows="5"
          placeholder="You can ask anything happens here message"
          class="w-full border border-gray-300 rounded-md p-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
        ></textarea>
      </div>

      <button
        type="submit"
        class="w-full bg-blue-600 text-white font-semibold py-3 rounded-md hover:bg-blue-700 transition duration-300"
      >
        Let’s talk
      </button>
    </form>
  </div>
</template>
