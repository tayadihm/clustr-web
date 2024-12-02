<template>
  <section class="hero" id="home">
    <div class="content" data-aos="fade-up">
      <h1>Hunian Nyaman untuk Keluarga Anda</h1>
      <p>
        Temukan rumah impian Anda di lokasi yang strategis dan fasilitas
        terbaik.
      </p>
      <button class="cta">Jelajahi Sekarang</button>
    </div>
  </section>
</template>

<style lang="scss">
.hero {
  background: url('https://source.unsplash.com/1600x900/?house') no-repeat
    center center/cover;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;

  .content {
    color: white;

    h1 {
      font-size: 3rem;
      text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
    }

    p {
      margin: 1rem 0;
      font-size: 1.2rem;
    }

    .cta {
      padding: 0.8rem 2rem;
      background-color: #4caf50;
      border: none;
      color: white;
      font-size: 1rem;
      cursor: pointer;
      transition: transform 0.3s;
      &:hover {
        transform: scale(1.1);
      }
    }
  }
}
</style>
