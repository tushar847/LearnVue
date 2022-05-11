<script setup>
import Navbar from '@/components/Navbar.vue';
import Footer from '@/components/Footer.vue';
import About from '@/components/About.vue';
import Home from '@/components/Home.vue';
import Questions from '@/components/Questions.vue';
import Contact from '@/components/Contact.vue';
import Product from '@/components/Product.vue';
import Steps from '@/components/Steps.vue';
</script>

<template>
  <Navbar />
  <main>
    <Home />
    <Steps/>
    <Product/>
    <Questions/>
    <Contact/>
  </main>
  <Footer />
</template>
