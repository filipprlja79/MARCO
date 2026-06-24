<script setup>
import { computed } from "vue";

import diplomaImg from "../assets/images/awards/diploma1.png";
import medalImg from "../assets/images/awards/medalja1.png";
import { currentLanguage } from "../data/languageStore";
import { translations } from "../data/translations";

import {
  Trophy,
  ShieldCheck,
  MapPinned
} from "lucide-vue-next";

const t = computed(() => translations[currentLanguage.value].awards);
</script>

<template>
  <section id="nagrade" class="awards">
    <div class="awards__container">
      <span class="awards__eyebrow">
        {{ t.eyebrow }}
      </span>

      <h2 class="header">
        {{ t.title }}
      </h2>

      <p class="awards__description">
        {{ t.description }}
      </p>

      <div class="award-card">
        <div class="award-card__image">
          <img
            class="award-card__diploma"
            :src="diplomaImg"
            :alt="t.diplomaAlt"
          />

          <div class="award-card__overlay">
            <img
              class="award-card__medal"
              :src="medalImg"
              :alt="t.medalAlt"
            />
          </div>
        </div>
      </div>

      <div class="awards__features">
        <div class="feature">
          <div class="feature__icon">
            <Trophy />
          </div>

          <div>
            <h4>{{ t.firstTitle }}</h4>
            <p>{{ t.firstText }}</p>
          </div>
        </div>

        <div class="feature">
          <div class="feature__icon">
            <ShieldCheck />
          </div>

          <div>
            <h4>{{ t.secondTitle }}</h4>
            <p>{{ t.secondText }}</p>
          </div>
        </div>

        <div class="feature">
          <div class="feature__icon">
            <MapPinned />
          </div>

          <div>
            <h4>{{ t.thirdTitle }}</h4>
            <p>{{ t.thirdText }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style src="../assets/styles/awards.css" scoped></style>