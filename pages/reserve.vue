<template>
  <div class="p-9">
    <!-- Reserveer sectie -->
    <section>
      <h2 class="text-2xl font-bold mb-4 text-blue-900">Reserve</h2>

      <div class="space-y-4">
        <div
          v-for="(item, index) in reserveItems"
          :key="index"
          class="flex bg-white rounded-xl shadow p-4 gap-4 items-start"
        >
          <img
            src="/images/5.jpg"
            alt="Book cover"
            class="w-32 h-32 object-cover rounded-md"
          />
          <div class="flex-1">
            <h3 class="text-blue-900 font-bold">{{ item.title }}</h3>
            <p class="text-sm text-gray-500 mb-2">{{ item.artist }}</p>
            <p class="text-sm text-gray-600 mb-4">{{ item.description }}</p>
            <div
              class="flex justify-between items-center text-sm text-gray-500"
            >
              <span>Tot {{ item.date }}</span>
              <div class="flex gap-2">
                <button
                  class="text-white bg-blue-500 px-3 py-1 rounded-md hover:bg-blue-600"
                >
                  Verleng
                </button>
                <button class="text-red-500">
                  <i class="fas fa-heart"></i>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Uitleeningen sectie -->
    <section class="mt-12">
      <h2 class="text-2xl font-bold mb-6 text-blue-900">Uitleeningen</h2>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div
          v-for="(item, index) in loanItems"
          :key="index"
          class="bg-white rounded-xl shadow p-4 flex flex-col"
        >
          <img
            src="/images/11.jpg"
            alt="Book cover"
            class="w-full h-48 object-cover rounded-md mb-4"
          />
          <h3 class="text-blue-900 font-bold mb-1">{{ item.title }}</h3>
          <p class="text-sm text-gray-500 mb-2">{{ item.artist }}</p>
          <p class="text-sm text-gray-600 flex-1 mb-4">
            {{ item.description }}
          </p>
          <div class="flex justify-between items-center mt-auto">
            <button
              class="text-blue-600 border border-blue-600 px-3 py-1 rounded hover:bg-blue-50"
            >
              Read more
            </button>
            <button class="text-blue-600"><i class="far fa-heart"></i></button>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const reserveItems = [
  {
    title: "Portrait of the artist",
    artist: "Artist",
    description:
      "Sed ut perspiciatis unde omnis iste ,. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iufugiat quo voluptas nulla pariatur?",

    date: "10.03.2024",
    image: "/images/5.jpg",
  },
  {
    title: "Portrait of the artist",
    artist: "Artist",
    description:
      "Sed ut perspiciatis unde o aut odit aut fugit,unt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur, vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?",

    date: "10.03.2024",
    image: "https://via.placeholder.com/150x150?text=Image2",
  },
];

const loanItems = Array(5).fill({
  title: "Portrait of the artist",
  artist: "Artist",
  description: "nam etiam egestas morbi feu... suspendisse donec lacus",
  image: "https://via.placeholder.com/200x300?text=Portrait",
});
</script>

<style scoped>
/* Voor icons zoals hartje */
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css");
</style>
