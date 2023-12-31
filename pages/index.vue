<template>
  <div>
    <!-- Le contenu spécifique à maPage.vue -->
    <gal />
  </div>
</template>
<script>
import gal from '/pages/component/galery.vue'; // Assurez-vous d'ajuster le chemin selon votre structure

export default {
  components: {
    gal,
  },
  layout: 'default',
};
</script>
