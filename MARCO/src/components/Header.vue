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
      <a href="#home" @click="isOpen = false">Home</a>
      <a href="#products" @click="isOpen = false">Products</a>
      <a href="#bestsellers" @click="isOpen = false">Bestsellers</a>
      <a href="#awards" @click="isOpen = false">Awards</a>
      <a href="#partners" @click="isOpen = false">Partners</a>
      <a href="#recipes" @click="isOpen = false">Ideas</a>
      <a href="#faq" @click="isOpen = false">FAQ</a>
      <a href="#contact" @click="isOpen = false">Contact</a>
    </nav>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import '../assets/styles/header.css'

const isOpen = ref(false)
</script>