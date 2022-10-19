<template>
  <HeaderComponent />
  <div class="bg-white">
    <main class="overflow-hidden">
      <FAQ />
      <ContactForm />
      <OfficesGrid />
    </main>
    <FooterComponent />
  </div>
</template>

<script setup>
import OfficesGrid from "./components/OfficesGrid.vue";
import ContactForm from "./components/ContactForm.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";
import FAQ from "./components/FAQ.vue";
</script>
