<template>
  <div>
    <Navbar />
    <Hero />
    <Features />
    <Gallery />
    <ContactForm />
    <Footer />
    <Home />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Features from './components/Features.vue';
import Gallery from './components/Gallery.vue';
import ContactForm from './components/ContactForm.vue';
import Footer from './components/Footer.vue';
import Home from './components/Home.vue';

export default {
  components: { Navbar, Hero, Features, Gallery, ContactForm, Footer, Home},
};
</script>
