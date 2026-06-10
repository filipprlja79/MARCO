<template>
  <section id="partners" class="partners">
    <div class="partners__container">
      <span class="partners__eyebrow">Istaknuti partneri</span>

      <h2>Gdje možete pronaći MARCO proizvode</h2>

      <p class="partners__lead">
        MARCO proizvodi dostupni su širom Crne Gore kroz mrežu naših partnera i
        prodajnih mjesta.
      </p>

      <div class="partners__grid">
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

      <p class="partners__bottom">
        Naši proizvodi svakodnevno stižu do mnogo kupaca kroz pažljivo
        odabranu mrežu partnera širom Crne Gore. Od velikih trgovinskih lanaca i
        aerodroma do lokalnih restorana, hotela i kafića. Kvalitet MARCO
        proizvoda prepoznat je na mjestima gdje se cijene tradicija i ukus.
      </p>
    </div>
  </section>
</template>

<script setup>
import "../assets/styles/partners.css";

const partners = [
  {
    name: "Voli Trade",
    logo: "../src/assets/images/partneri/Voli.png",
    description: "Jedan od vodećih maloprodajnih lanaca u Crnoj Gori.",
  },
  {
    name: "Domaća Trgovina",
    logo: "../src/assets/images/partneri/Domaca-trgovina.png",
    description: "Aroma, City i Conto marketi.",
  },
  {
    name: "Jugopetrol",
    logo: "../src/assets/images/partneri/Eko.png",
    description: "Prodajna mreža kroz EKO/Jugopetrol objekte.",
  },
  {
    name: "Mega Market",
    logo: "../src/assets/images/partneri/Mega-market.png",
    description: "Mega marketi Budva.",
  },
  {
    name: "Aerodromi Crne Gore",
    logo: "../src/assets/images/partneri/Aerodromi-CG.png",
    description: "Prisustvo na važnim putnim tačkama Crne Gore.",
  },
];
</script>