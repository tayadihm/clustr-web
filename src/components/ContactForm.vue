<template>
  <section id="contact" class="contact">
    <h2>Hubungi Kami</h2>
    <form @submit.prevent="handleSubmit">
      <div>
        <label for="name">Nama:</label>
        <input type="text" id="name" v-model="form.name" required />
      </div>
      <div>
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="form.email" required />
      </div>
      <div>
        <label for="message">Pesan:</label>
        <textarea id="message" v-model="form.message" required></textarea>
      </div>
      <button type="submit">Kirim</button>
    </form>
    <p v-if="message" class="success">{{ message }}</p>
  </section>
</template>

<script>
export default {
  name: 'ContactForm',
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: '',
      },
      message: '',
    };
  },
  methods: {
    async handleSubmit() {
      try {
        const response = await fetch('http://localhost:5000/api/contact', {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json',
          },
          body: JSON.stringify(this.form),
        });
        if (response.ok) {
          this.message = 'Pesan berhasil dikirim!';
          this.form = { name: '', email: '', message: '' };
        } else {
          this.message = 'Gagal mengirim pesan. Coba lagi nanti.';
        }
      } catch (error) {
        this.message = 'Terjadi kesalahan. Silakan coba lagi.';
        console.error(error);
      }
    },
  },
};
</script>

<style scoped>
.contact {
  max-width: 600px;
  margin: auto;
  padding: 20px;
  background-color: #fff;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
}
.contact form div {
  margin-bottom: 15px;
}
.contact label {
  display: block;
  font-weight: bold;
  margin-bottom: 5px;
}
.contact input,
.contact textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}
.contact button {
  background-color: #4caf50;
  color: white;
  padding: 10px 15px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
.contact button:hover {
  background-color: #45a049;
}
.success {
  margin-top: 10px;
  color: green;
  font-weight: bold;
}
</style>
