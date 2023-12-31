<template>
  <div>
    <header>
      <div class="header-content">
        <!-- Logo on the left -->
        <NuxtLink to="/" class="logo-link">
          <img src="/logo.png" alt="Mon Site Web Logo" class="logo" />
        </NuxtLink>

        <!-- Bouton Hamburger -->

        <!-- Navigation component (caché par défaut) -->
        <div>
          <Nav />
        </div>
      </div>
    </header>

    <main>
      <nuxtPage />
    </main>

    <footer>
      <div class="header-content foot">
        <!-- Logo on the left -->
        <NuxtLink to="/" class="logo-link">
          <img src="/logo.png" alt="Mon Site Web Logo" class="logo" />
        </NuxtLink>

        <!-- Bouton Hamburger -->

        <!-- Navigation component (caché par défaut) -->
        <div>
          <Nav />
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import Nav from '/pages/component/nav.vue'; // Ajustez le chemin selon votre structure

export default {
  components: {
    Nav,
  },
  data() {
    return {
      isMenuActive: false, // État initial du menu
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuActive = !this.isMenuActive;
    },
  },
};
</script>

<style scoped>
/* ... autres styles ... */

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
}
.foot {
  display: flex;
  justify-content: space-evenly;
  align-items: center;

  background-color: #edede9;
}
.foot .logo {
  max-height: 75px;
}

.logo {
  /* Ajustez la taille du logo comme nécessaire */
  height: auto;
  max-height: 150px; /* Exemple de taille */
}

/* Bouton hamburger caché sur les grands écrans et affiché sur les petits écrans */
.hamburger {
  display: none; /* Caché sur les écrans plus larges que 768px */
}

/* Style pour votre composant Nav */
.nav {
  display: flex;
  align-items: center;
  /* Assurez-vous que votre composant Nav n'a pas de styles qui l'empêchent de s'afficher en ligne */
}

/* Style pour l'état actif du menu hamburger */
.menu-active {
  display: block;
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  background-color: white; /* Choisir une couleur de fond appropriée */
}

/* Styles pour mobile */
@media (max-width: 768px) {
  .header-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
    flex-direction: column;
  }
}

/* ... autres styles ... */
</style>
