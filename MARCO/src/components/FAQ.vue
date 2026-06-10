<template>
  <section class="faq" id="faq">
    <div class="faq__container">
      <div class="faq__header">
        <span class="faq__eyebrow">Često postavljana pitanja</span>
        <h2>FAQ</h2>
        <p>
          Odgovori na najčešća pitanja o MARCO proizvodima,
          proizvodnji i naručivanju.
        </p>
      </div>

      <div class="faq__list">
        <div
          class="faq__item"
          :class="{ 'faq__item--open': openItems.includes(index) }"
          v-for="(item, index) in faqs"
          :key="index"
        >
          <button
            class="faq__question"
            type="button"
            @click="toggle(index)"
          >
            <span>{{ item.question }}</span>

            <span class="faq__icon">
              <span></span>
              <span></span>
            </span>
          </button>

          <div
            class="faq__answer-wrap"
            :class="{ 'faq__answer-wrap--open': openItems.includes(index) }"
          >
            <div class="faq__answer">
              <p>{{ item.answer }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const openItems = ref([]);

const toggle = (index) => {
  if (openItems.value.includes(index)) {
    openItems.value = openItems.value.filter((item) => item !== index);
  } else {
    openItems.value.push(index);
  }
};

const faqs = [
  {
    question: "Odakle dolazi meso koje koristite?",
    answer:
      "Za proizvodnju koristimo pažljivo odabrano meso provjerenog porijekla kako bismo osigurali vrhunski kvalitet svakog proizvoda.",
  },
  {
    question: "Kako se proizvodi MARCO pršuta?",
    answer:
      "MARCO proizvodi nastaju tradicionalnim dimljenjem i prirodnim procesom zrenja, uz pažljivo kontrolisane uslove proizvodnje.",
  },
  {
    question: "Da li vršite dostavu proizvoda?",
    answer:
      "Za informacije o dostavi i dostupnosti proizvoda možete nas kontaktirati putem kontakt forme ili telefona.",
  },
  {
    question: "Gdje mogu kupiti MARCO proizvode?",
    answer:
      "Naše proizvode možete pronaći kod odabranih partnera širom Crne Gore, uključujući markete, benzinske stanice i ugostiteljske objekte.",
  },
  {
    question: "Da li proizvodi sadrže alergene?",
    answer:
      "Za detaljne informacije o sastavu i alergenima pogledajte deklaraciju proizvoda ili nas kontaktirajte direktno.",
  },
];
</script>

<style scoped>
@import "../assets/styles/FAQ.css";
</style>