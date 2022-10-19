<template>
  <HeaderComponent />
  <div class="bg-white">
    <main class="overflow-hidden">
      <FAQ />
      <div class="bg-stone-50">
        <div class="py-24 lg:py-32">
          <div
            class="relative z-10 mx-auto max-w-7xl pr-8 pl-4 sm:px-6 lg:px-8"
          >
            <h1
              class="text-4xl font-bold tracking-tight text-stone-900 sm:text-5xl lg:text-6xl"
            >
              Get in touch
            </h1>
            <p class="mt-6 max-w-3xl text-xl text-stone-500">
              Vel nunc non ut montes, viverra tempor. Proin lectus nibh
              phasellus morbi non morbi. In elementum urna ut volutpat. Sagittis
              et vel et fermentum amet consequat.
            </p>
          </div>
        </div>
      </div>
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
