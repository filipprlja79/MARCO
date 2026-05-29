<template>
  <section id="contact" class="contact">
    <div class="contact__container">

      <div class="contact__info">
        <span class="contact__subtitle">kONTAKTIRAJTE NAS</span>

        <h2 class="contact__title">
          Imate pitanja ili želite da sarađujete sa nama?
        </h2>

        <p class="contact__description">
          Zainteresovani ste za naše proizvode ili imate pitanja? Kontaktirajte nas putem obrasca  ili putem naših kontakt informacija. Radujemo se vašem javljanju!
        </p>

        <p class="contact__description">
          <strong>Email:</strong> markovujovic@gmail.com
        </p>

      </div>

      <form class="contact__form">
        <input
          type="text"
          placeholder="Your Name"
          class="contact__input"
        >

        <input
          type="email"
          placeholder="Your Email"
          class="contact__input"
        >

        <input
          type="tel"
          placeholder="Phone Number"
          class="contact__input"
        >

        <textarea
          rows="6"
          placeholder="Your Message"
          class="contact__textarea"
        ></textarea>

        <button
          type="submit"
          class="contact__button"
        >
          Pošalji
        </button>
      </form>

    </div>
  </section>
</template>

<script setup>
import '../assets/styles/contact.css'
</script>