<template>
  <section class="products" id="products">
    <div class="products__container">
      <div class="products__header">
        <span class="products__eyebrow">MARCO proizvodi</span>
        <h2>Ukus tradicije u svakom komadu</h2>
        <p>
          Pažljivo birani suhomesnati specijaliteti, pripremljeni tradicionalnim
          postupkom dimljenja, soljenja i prirodnog zrenja.
        </p>
      </div>

      <div class="products__grid products__desktop">
        <article
          v-for="product in products"
          :key="product.name"
          class="product-card"
        >
          <div class="product-card__image">
            <img :src="product.image" :alt="product.name" />
          </div>

          <div class="product-card__content">
            <span class="product-card__tag">{{ product.tag }}</span>
            <h3>{{ product.name }}</h3>
            <p>{{ product.description }}</p>
          </div>
        </article>
      </div>

      <Swiper
        class="products__mobile"
        :slides-per-view="1.12"
        :space-between="18"
        :centered-slides="true"
        :grab-cursor="true"
      >
        <SwiperSlide
          v-for="product in products"
          :key="product.name"
        >
          <article class="product-card">
            <div class="product-card__image">
              <img :src="product.image" :alt="product.name" />
            </div>

            <div class="product-card__content">
              <span class="product-card__tag">{{ product.tag }}</span>
              <h3>{{ product.name }}</h3>
              <p>{{ product.description }}</p>
            </div>
          </article>
        </SwiperSlide>
      </Swiper>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";

import suviVrat from "../assets/images/suvi vrat.jpg";
import pakovanjePrsute from "../assets/images/pakovanje prsute.jpg";
import pakovanjePanceta from "../assets/images/pakovanje panceta.jpg";
import amanetPakovanje from "../assets/images/Amanet pakovanje.jpg";
import suvaPecenica from "../assets/images/suva pecenica.jpg";
import njeguskiPrsut from "../assets/images/njeguski prsut.jpg";
import njeguskaPecenica from "../assets/images/njeguska pecenica.jpg";
import slanina from "../assets/images/slanina.jpg";

const products = [
  {
    name: "Njeguški suvi vrat",
    tag: "Selection",
    image: suviVrat,
    description:
      "Pun, dimljen i bogat ukus za one koji traže pravi karakter tradicionalnog suhomesnatog proizvoda.",
  },
  {
    name: "Pakovanje crnogorskog pršuta",
    tag: "Premium pakovanje",
    image: pakovanjePrsute,
    description:
      "Elegantno rezano pakovanje pršuta, spremno za posluženje, poklon ili premium ugostiteljsku ponudu.",
  },
  {
    name: "Pakovanje pancete",
    tag: "Premium pakovanje",
    image: pakovanjePanceta,
    description:
      "Sočna panceta u modernom pakovanju, idealna za meze, sendviče, doručak i specijalitete sa punim ukusom.",
  },
  {
    name: "Amanet suvi goveđi pršut",
    tag: "Amanet linija",
    image: amanetPakovanje,
    description:
      "Posebna linija proizvoda koja spaja nasljeđe, kvalitet i ukus namijenjen pravim ljubiteljima delikatesa.",
  },
  {
    name: "Suva pečenica",
    tag: "Tradicionalni specijalitet",
    image: suvaPecenica,
    description:
      "Nježna, aromatična i pažljivo dimljena pečenica, odlična za svakodnevno posluženje i posebne prilike.",
  },
  {
    name: "Njeguški pršut",
    tag: "Klasik",
    image: njeguskiPrsut,
    description:
      "Prepoznatljiv crnogorski specijalitet, sušen i zren po tradicionalnom postupku za autentičan ukus.",
  },
  {
    name: "Njeguška pečenica",
    tag: "Selection",
    image: njeguskaPecenica,
    description:
      "Kvalitetan komad mesa sa blagim dimljenim notama i teksturom koja se lako uklapa u svako jelo.",
  },
  {
    name: "Slanina",
    tag: "Domaći ukus",
    image: slanina,
    description:
      "Tradicionalna slanina bogate arome, idealna za domaću trpezu, roštilj, doručak i kuvana jela.",
  },
];
</script>

<style scoped>
@import "../assets/styles/products.css";
</style>