<template>
  <section id="gallery">
    <h2 data-aos="fade-up">Galeri</h2>
    <div class="gallery-grid">
      <img
        v-for="(image, index) in images"
        :key="index"
        :src="image"
        alt="Gallery"
        data-aos="zoom-in"
      />
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      images: [
        'https://source.unsplash.com/300x200/?house',
        'https://source.unsplash.com/300x200/?villa',
        'https://source.unsplash.com/300x200/?modern-house',
        'https://source.unsplash.com/800x600/?minimalist-house',
      ],
    };
  },
};
</script>

<style lang="scss">
[data-aos] {
  opacity: 0;
  transition: opacity 0.6s ease-out;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
  margin: 1rem 0;

  @media (max-width: 600px) {
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  }

  img {
    width: 100%;
    height: auto;
    border-radius: 10px;
    transition: transform 0.3s;
    &:hover {
      transform: scale(1.1);
    }
  }
}
</style>
