<template>
    <section id="features">
      <div class="feature" v-for="(feature, index) in features" :key="index" data-aos="zoom-in">
        <h3>{{ feature.title }}</h3>
        <p>{{ feature.description }}</p>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        features: [
          { title: 'Lokasi Strategis', description: 'Dekat dengan fasilitas umum dan transportasi.' },
          { title: 'Fasilitas Lengkap', description: 'Kolam renang, taman bermain, dan keamanan 24 jam.' },
          { title: 'Harga Terjangkau', description: 'Dapatkan rumah impian Anda dengan harga terbaik.' },
        ],
      };
    },
  };
  </script>
  
  <style lang="scss">
  #features {
    display: flex;
    justify-content: space-around;
    padding: 2rem 0;
  
    .feature {
      text-align: center;
      max-width: 300px;
  
      h3 {
        color: #4caf50;
        margin-bottom: 0.5rem;
      }
    }
  }
  </style>
  