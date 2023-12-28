<template>
  <header class="header">
    <img class="header__logo" src="/images/logo.svg" alt="LOGO" />
    <button class="header__menu">
      <img class="header__menu__icon" src="/images/icon/menu.svg">
    </button>
  </header>

  <main>
    <h1 class="page__title">Page 1</h1>
    
    <section class="section feature">
      <h2 class="section__title">Feature</h2>
      <ul class="feature__list">
        <li v-for="index in 4" class="feature__list__item">
          <img :src="`/images/feature/img_${index}.png`" :alt="`feature${index}`">
          <h3 class="feature__list__item__title">Title</h3>
          <p class="feature__list__item__description">I am description. I am description. I am description.</p>
          <small class="feature__list__item__annotation">I am annotation. I am annotation. I am annotation.</small>
        </li>
      </ul>
    </section>
    
    <section class="section contact">
      <h2 class="section__title">Contact</h2>
      <div class="formGroup">
        <label for="name">Your Name</label>
        <input type="text" v-model="contactForm.name" />
      </div>
      <div class="formGroup">
        <label for="name">Comment</label>
        <textarea v-model="contactForm.comment" />
      </div>
      <button @click="submitForm">Submit Form</button>
    </section>
  </main>
</template>

<script setup lang="ts">
const contactForm = reactive({
  name: "",
  comment: "",
})

const submitForm = () => {
  console.log(contactForm)
}
</script>

<style lang="scss">
</style>