<template>
  <header class="header">
    

    <button
  class="header__toggle"
  :class="{ 'header__toggle--open': isOpen }"
  @click="isOpen = !isOpen"
>
  <span></span>
  <span></span>
  <span></span>
</button>

    <nav class="nav" :class="{ 'nav--open': isOpen }">
      <a href="#home" @click="isOpen = false">Početna</a>
      <a href="#products" @click="isOpen = false">Proizvodi</a>
      <a href="#bestsellers" @click="isOpen = false">Najprodavaniji</a>
      <a href="#awards" @click="isOpen = false">Nagrade</a>
      <a href="#partners" @click="isOpen = false">Partneri</a>
      <a href="#recipes" @click="isOpen = false">Ideje</a>
      
      <a href="#faq" @click="isOpen = false">FAQ</a>
      <a href="#contact" @click="isOpen = false">Kontakt</a>
    </nav>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import '../assets/styles/header.css'

const isOpen = ref(false)
</script>