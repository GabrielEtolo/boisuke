<template>
  <div class="gallery">
    <div class="top-section">
      <!-- Conteneur pour Photo 3 et texte -->
      <div class="image image3">
        <img :src="`/${images[0]}`" alt="Gallery image 3" />
      </div>
    </div>
    <div class="image-row">
      <div
        class="image"
        :class="getImageClass(index)"
        v-for="(image, index) in images.slice(1)"
        :key="index"
      >
        <img :src="`/${image}`" alt="Gallery image" />
        <div class="texte">{{ texte[index] }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        'boisuke.png',
        'gen.JPG',
        'anton.JPG',
        'gen2.JPG',
        'anton2.JPG',
        'dinero.JPG',
        'manon.jpg',
        'dinero2.jpg',
        'Isaac.jpg',
      ],
      texte: [
        'Plongez dans Boisuke',
        'Sensibilité Boi',
        'Esthétique GEN',
        'Vision LB',
        'Un magasine',
        'Authentique',
        'Jeune',
        'Bruxellois',
      ],
    };
  },
  methods: {
    getImageClass(index) {
      // Cette méthode retourne 'image1' pour les indices pairs et 'image2' pour les indices impairs
      return index % 2 === 0 ? 'image1' : 'image2';
    },
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@1&display=swap');

.gallery {
  max-width: 1200px;
  margin: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.top-section {
  display: flex;
  width: 100%;
  flex-direction: row-reverse;
  justify-content: center;
  align-items: flex-start;
  margin-bottom: 20px;
}

.image3 {
  width: 50%;
  position: relative;
}

.text-content {
  width: 50%; /* Le texte prend l'autre moitié de la largeur */
  padding-right: 100px; /* Un peu d'espace entre le texte et l'image */
  font-family: 'Roboto', sans-serif;
  font-size: xx-large;
  line-height: 200%;
}
.text-content i {
  font-family: 'Carattere', cursive;
  color: #f00;
  font-size: xxx-large;
}

.image-row {
  display: flex;
  width: 100%;
  justify-content: center;
  flex-direction: column;
}

.image-column {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}

.image {
  position: relative;
  margin-bottom: 20px;
  width: fit-content;
  transition: transform 0.3s ease;
  display: flex;
  align-items: center;
}
.image .texte {
  padding: 5%;
}

.image img {
  width: 100%;
  display: block;
  border-radius: 20px;
  -webkit-box-shadow: 2px 4px 37px -19px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: 2px 4px 37px -19px rgba(0, 0, 0, 0.75);
  box-shadow: 2px 4px 37px -19px rgba(0, 0, 0, 0.75);
  transition: 0.5s;
}

.image img:hover {
  transform: scale(1.03);
}

.image1 {
  width: fit-content%;
  align-self: flex-start;
}
.image1 img {
  width: 40%;
  align-self: flex-start;
}

.image2 {
  width: 100%;
  align-self: flex-end;
  flex-direction: row-reverse;
}
.image2 img {
  width: 60%;
}
.image3 img {
  height: 450px;
  width: 100%;
}
.texte {
  font-family: 'DM Serif Display', serif;
  font-size: 50px;
  color: #f3676f;
}
</style>
