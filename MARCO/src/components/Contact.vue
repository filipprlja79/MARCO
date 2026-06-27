<template>
  <section id="contact" class="contact">
    <div class="contact__container">

      <div class="contact__info">
        <span class="contact__subtitle">
          {{ t.subtitle }}
        </span>

        <h2 class="contact__title">
          {{ t.title }}
        </h2>

        <p class="contact__description">
          {{ t.description }}
        </p>

        <p class="contact__description">
          <strong>{{ t.emailLabel }}</strong>
          markovujovic@gmail.com
        </p>
      </div>

      <form class="contact__form">
        <input
          type="text"
          :placeholder="t.namePlaceholder"
          class="contact__input"
        >

        <input
          type="email"
          :placeholder="t.emailPlaceholder"
          class="contact__input"
        >

        <input
          type="tel"
          :placeholder="t.phonePlaceholder"
          class="contact__input"
        >

        <textarea
          rows="6"
          :placeholder="t.messagePlaceholder"
          class="contact__textarea"
        ></textarea>

        <button
          type="submit"
          class="contact__button"
        >
          {{ t.button }}
        </button>
      </form>

    </div>
  </section>
</template>

<script setup>
import { computed } from "vue";
import "../assets/styles/contact.css";

import { currentLanguage } from "../data/languageStore";
import { translations } from "../data/translations";

const t = computed(() => {
  return translations[currentLanguage.value].contact;
});
</script>