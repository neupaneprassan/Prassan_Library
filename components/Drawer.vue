<script setup lang="ts">
import { onMounted } from "vue";
import { Drawer } from "flowbite";
import Menu from "vue-material-design-icons/Menu.vue";

onMounted(() => {
  const $targetEl = document.getElementById("drawer-swipe");
  const $drawerHideButton = document.getElementById("drawer-hide-button");
  const $drawerShowButton = document.getElementById("drawer-show-button");

  const navLinks = document.querySelectorAll("#drawer-swipe nav a");

  navLinks.forEach((link) => {
    if (link.getAttribute("href") === window.location.pathname) {
      link.classList.add("active");
    }

    link.addEventListener("click", () => {
      navLinks.forEach((l) => l.classList.remove("active"));
      link.classList.add("active");
    });
  });

  const options = {
    placement: "left",
    backdrop: true,
    bodyScrolling: true,
    edge: false,
    edgeOffset: "",
    backdropClasses:
      "bg-zinc-100 dark:bg-zinc-900 bg-opacity-90 dark:bg-opacity-80 fixed inset-0 z-30",
    onHide: () => {},
    onShow: () => {},
    onToggle: () => {},
  };

  if ($targetEl) {
    const drawer = new Drawer($targetEl, options);
    drawer.hide();
    $drawerHideButton?.addEventListener("click", () => drawer.hide());
    $drawerShowButton?.addEventListener("click", () => drawer.show());
  }
});
</script>

<template>
  <div class="drawer-header">
    <button id="drawer-show-button" type="button" aria-controls="drawer-swipe">
      <Menu :size="30" />
    </button>
    <img src="/images/NEW_LOGO.png" alt="BSLB Logo" class="logo-img" />
    <div class="search-container">
      <input type="text" placeholder="Search" />
    </div>

    <div class="user-info flex items-center gap-4">
      <span class="text-white">Hallo Prassan_student</span>
      <NuxtLink to="/profile" class="text-white hover:text-blue-300">
        <i class="fas fa-user cursor-pointer"></i>
      </NuxtLink>
      <NuxtLink to="/mail" class="text-white hover:text-blue-300">
        <i class="fas fa-bell cursor-pointer"></i>
      </NuxtLink>
    </div>
  </div>

  <!-- Drawer Content -->
  <div
    id="drawer-swipe"
    class="fixed top-0 left-0 z-40 h-screen p-4 overflow-y-auto flex flex-col"
    tabindex="-1"
    aria-labelledby="drawer-label"
  >
    <!-- Close Button -->
    <button id="drawer-show-button" type="button" aria-controls="drawer-swipe">
      <Menu :size="30" />
      <span aria-hidden="true" class="sr-only">Close menu</span>
    </button>

    <!-- Navigation Links -->
    <nav class="mt-10 flex flex-col gap-4">
      <a
        href="/"
        class="flex items-center gap-3 text-gray-700 hover:bg-gray-100 rounded-lg p-2"
      >
        <i class="fas fa-home"></i> Homepage
      </a>
      <a
        href="/favoriet"
        class="flex items-center gap-3 text-gray-700 hover:bg-gray-100 rounded-lg p-2"
      >
        <i class="fas fa-heart"></i> Favoriet
      </a>
      <a
        href="/reserve"
        class="flex items-center gap-3 text-gray-700 hover:bg-gray-100 rounded-lg p-2"
      >
        <i class="fas fa-calendar-check"></i> Reserve
      </a>
      <a
        href="/news"
        class="flex items-center gap-3 text-gray-700 hover:bg-gray-100 rounded-lg p-2"
      >
        <i class="fas fa-newspaper"></i> News
      </a>
      <a
        href="#"
        class="flex items-center gap-3 text-gray-700 hover:bg-gray-100 rounded-lg p-2"
      >
        <i class="fas fa-cog"></i> Collectie
      </a>
      <a
        href="#"
        class="flex items-center gap-3 text-gray-700 hover:bg-gray-100 rounded-lg p-2"
      >
        <i class="fas fa-sign-out-alt"></i> Log out
      </a>
    </nav>

    <hr class="my-4" />

    <!-- Contact Block -->
    <div class="contact">
      <div class="flex items-center gap-2 text-gray-500 text-sm mt-6 ml-2">
        <i class="fas fa-user"></i> Contact
      </div>

      <!-- Language Switch -->
      <div class="flex gap-4 mt-3 ml-2 text-blue-700 text-sm">
        <a href="#">Engels</a>
        <a href="#">Dutch</a>
        <a href="#">French</a>
      </div>
      <ColorMode />
    </div>
  </div>
</template>

<style>
#drawer-swipe {
  background-color: rgb(255, 255, 255);
  width: 30vw;
}
.dark-mode #drawer-swipe {
  background-color: rgba(22, 23, 21, 0.95);
}
hr {
  border-color: #0091c6;
}
.dark-mode hr {
  border-color: aliceblue;
}
.contact {
  size: 4em;
}
.logo-img {
  max-width: 3%;
  margin-right: 30vw;
}
.user-info {
  margin-right: 10vw;
}
</style>
