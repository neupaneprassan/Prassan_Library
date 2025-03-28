<template>
  <div class="container">
    <h1 class="text-5xl font-semibold">{{ translations[language].welcome }}</h1>
    <p>{{ translations[language].message }}</p>
    <button @click="goToLogin" class="btn">
      {{ translations[language].login }}
    </button>
    <button @click="goToSignup" class="btn">
      {{ translations[language].signup }}
    </button>

    <!-- Taalwisselaar onderaan -->
    <div class="language-switcher">
      <button @click="changeLanguage('en')">🇬🇧</button>
      <button @click="changeLanguage('nl')">🇳🇱</button>
      <button @click="changeLanguage('fr')">🇫🇷</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      language: "en", // Standaardtaal is Engels
      translations: {
        en: {
          welcome: "Welcome",
          message: "Enter your email to sign up for this app",
          login: "Log in",
          signup: "Sign up",
        },
        nl: {
          welcome: "Welkom",
          message: "Voer je e-mail in om je aan te melden voor deze app",
          login: "Inloggen",
          signup: "Registreren",
        },
        fr: {
          welcome: "Bienvenue",
          message: "Entrez votre e-mail pour vous inscrire à cette application",
          login: "Se connecter",
          signup: "S'inscrire",
        },
      },
    };
  },
  methods: {
    goToLogin() {
      window.location.href = "http://localhost:3000/login";
    },
    goToSignup() {
      window.location.href = "http://localhost:3000/signup";
    },
    changeLanguage(lang) {
      this.language = lang;
    },
  },
};
</script>

<style>
.container {
  text-align: center;
  margin: 50px auto;
  max-width: 400px;
  padding: 20px;
}
.btn {
  display: block;
  width: 100%;
  margin: 10px 0;
  padding: 10px;
  background-color: black;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}
.btn:hover {
  background-color: #333;
}
.language-switcher {
  margin-top: 20px;
}
.language-switcher button {
  font-size: 20px;
  margin: 5px;
  background: none;
  border: none;
  cursor: pointer;
}
</style>
