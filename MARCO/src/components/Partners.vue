<template>
  <section id="partners" class="partners">
    <div class="partners__container">
      <span class="partners__eyebrow">{{ t.eyebrow }}</span>

      <h2 class = "header">{{ t.title }}</h2>

      <p class="partners__lead">
        {{ t.description }}
      </p>

      <div class="partners__grid partners__desktop">
        <article
          v-for="partner in partners"
          :key="partner.name"
          class="partners__item"
        >
          <img :src="partner.logo" :alt="partner.name" />
          <h3>{{ partner.name }}</h3>
          <p>{{ partner.description }}</p>
        </article>
      </div>

      <Swiper
        class="partners__mobile"
        :slides-per-view="1.15"
        :space-between="16"
        :centered-slides="true"
        :grab-cursor="true"
        :loop="true"
        :autoplay="{
    delay: 3000,
    disableOnInteraction: false
  }"
        
      >
        <SwiperSlide
          v-for="partner in partners"
          :key="partner.name"
        >
          <article class="partners__item">
            <img :src="partner.logo" :alt="partner.name" />
            <h3>{{ partner.name }}</h3>
            <p>{{ partner.description }}</p>
          </article>
        </SwiperSlide>
      </Swiper>

      <p class="partners__bottom">
        {{ t.bottom }}<br> <br>
        <a
    class="partners__location"
    href="https://maps.app.goo.gl/EzSMrhyW2HZVoZ5i9"
    target="_blank"
    rel="noopener noreferrer"
  >
  
   <span class="partners__pin">📍</span> {{ t.location }}
    
  </a>
      </p>
      
    </div>
  </section>
</template>

<script setup>
import { computed } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import { Autoplay } from "swiper/modules";
import "../assets/styles/partners.css";

import { currentLanguage } from "../data/languageStore";
import { translations } from "../data/translations";

import voliLogo from "../assets/images/partneri/Voli.png";
import domacaLogo from "../assets/images/partneri/Domaca-trgovina.png";
import jugopetrolLogo from "../assets/images/partneri/Eko.png";
import megaLogo from "../assets/images/partneri/Mega-market.png";
import aerodromiLogo from "../assets/images/partneri/Aerodromi-CG.png";

const t = computed(() => {
  return translations[currentLanguage.value].partners;
});

const partners = computed(() => {
  return [
    {
      name: t.value.items.voli.name,
      logo: voliLogo,
      description: t.value.items.voli.description,
    },
    {
      name: t.value.items.domaca.name,
      logo: domacaLogo,
      description: t.value.items.domaca.description,
    },
    {
      name: t.value.items.jugopetrol.name,
      logo: jugopetrolLogo,
      description: t.value.items.jugopetrol.description,
    },
    {
      name: t.value.items.mega.name,
      logo: megaLogo,
      description: t.value.items.mega.description,
    },
    {
      name: t.value.items.aerodromi.name,
      logo: aerodromiLogo,
      description: t.value.items.aerodromi.description,
    },
  ];
});
</script>