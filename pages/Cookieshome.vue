<template>
  <transition name="fade">
    <div
      v-if="visible"
      class="fixed inset-0 z-50 bg-black bg-opacity-70 flex items-center justify-center"
    >
      <div
        class="bg-[#1c1c1e] text-white max-w-md w-full mx-4 rounded-xl p-6 shadow-xl border border-gray-700"
      >
        <h2 class="text-lg font-semibold mb-4">
          {{
            locale === "nl"
              ? "Sta het gebruik van cookies van Bibliotheek Sint-Lukas Brussel toe in deze browser?"
              : "Allow the use of cookies from the Sint-Lukas Brussels Library on this browser?"
          }}
        </h2>

        <div
          class="max-h-60 overflow-y-auto text-sm text-gray-300 space-y-4 pr-2"
        >
          <p v-if="locale === 'en'">
            We use cookies and similar technologies to improve the experience on
            our Library website. Cookies help us remember your preferences (like
            language or accessibility settings), and to offer useful features
            such as saving your search history or maintaining login sessions.
          </p>
          <p v-else>
            Wij gebruiken cookies en gelijkaardige technologieën om de ervaring
            op onze bibliotheekwebsite te verbeteren. Cookies helpen ons om jouw
            voorkeuren te onthouden (zoals taal of
            toegankelijkheidsinstellingen) en om nuttige functies aan te bieden
            zoals het bewaren van zoekgeschiedenis of login-sessies.
          </p>

          <ul class="list-disc list-inside space-y-2">
            <li v-if="locale === 'en'">
              <strong>Essential cookies:</strong> These are necessary for the
              website to function properly and cannot be turned off. They help
              with security, accessibility, and core navigation.
            </li>
            <li v-else>
              <strong>Essentiële cookies:</strong> Deze zijn noodzakelijk om de
              website goed te laten functioneren en kunnen niet worden
              uitgeschakeld. Ze zorgen voor veiligheid, toegankelijkheid en
              basisnavigatie.
            </li>

            <li v-if="locale === 'en'">
              <strong>Functional & analytics cookies:</strong> These allow us to
              analyze how visitors use our site (e.g. most viewed pages), and
              improve the performance and usability of the platform.
            </li>
            <li v-else>
              <strong>Functionele & analytische cookies:</strong> Deze cookies
              helpen ons te begrijpen hoe bezoekers onze site gebruiken (bijv.
              meest bezochte pagina’s), en verbeteren de prestaties en
              bruikbaarheid van het platform.
            </li>
          </ul>

          <p v-if="locale === 'en'">
            You can choose whether to allow optional cookies. Learn more in our
            <span class="underline cursor-pointer">Cookies Policy</span>, or
            adjust your settings at any time. See our
            <span class="underline cursor-pointer">Privacy Policy</span> for
            more details.
          </p>
          <p v-else>
            Je kunt ervoor kiezen om optionele cookies toe te staan. Meer info
            vind je in ons
            <span class="underline cursor-pointer">cookiebeleid</span>, of je
            kunt je voorkeuren op elk moment aanpassen. Bekijk ook ons
            <span class="underline cursor-pointer">privacybeleid</span> voor
            meer informatie.
          </p>
        </div>

        <div class="border-t border-gray-700 my-4"></div>

        <!-- Knoppen -->
        <div class="flex justify-between gap-4">
          <button
            class="bg-[#2c2c2e] text-white py-2 px-4 rounded-lg hover:bg-[#3a3a3c] text-sm w-full"
            @click="declineCookies"
          >
            {{
              locale === "nl"
                ? "Weiger optionele cookies"
                : "Decline optional cookies"
            }}
          </button>
          <button
            class="bg-white text-black py-2 px-4 rounded-lg hover:bg-gray-100 text-sm w-full font-medium"
            @click="acceptCookies"
          >
            {{
              locale === "nl" ? "Alle cookies toestaan" : "Allow all cookies"
            }}
          </button>
        </div>
      </div>
    </div>
  </transition>
</template>

<script setup>
import { ref } from "vue";
import { useRouter, useRoute } from "vue-router";
const visible = ref(true);
const router = useRouter();
const route = useRoute();

const locale = route.params.lang || "en";

const acceptCookies = () => {
  useCookie("cookies-accepted").value = "all";
  visible.value = false;

  // Navigeer naar index.vue (bijv. naar /home of /)
  router.push({ name: "index" }); // Zorg dat je route zo heet
};

const declineCookies = () => {
  useCookie("cookies-accepted").value = "essential";
  visible.value = false;
  // Navigeer naar index.vue (bijv. naar /home of /)
  router.push({ name: "index" }); // Zorg dat je route zo heet
};
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.bg-black {
  background-color: #0a2b8c;
}
</style>
