<template>
  <header class="header">
    <div class="header__contents">
      <img class="header__logo" src="/images/logo.svg" alt="LOGO" />
      <button class="header__menu">
        <img class="header__menu__icon" src="/images/icon/menu.svg">
      </button>
    </div>
  </header>

  <main class="page">
    <h1 class="page__title">Page 1</h1>
    
    <section class="section feature">
      <h2 class="section__title">
        <img class="section__title__icon" src="/images/icon/flag.svg">
        Feature
      </h2>
      <ul class="feature__list">
        <li v-for="index in 4" class="feature__list__item">
          <img class="feature__list__item__img" :src="`/images/feature/img_${index}.png`" :alt="`feature${index}`">
          <hr />
          <h3 class="feature__list__item__title">Title</h3>
          <p class="feature__list__item__description">I am description. I am description. I am description.</p>
          <small class="feature__list__item__annotation">I am annotation. I am annotation. I am annotation.</small>
        </li>
      </ul>
    </section>
    
    <section class="section contact">
      <h2 class="section__title">
        <img class="section__title__icon" src="/images/icon/question.svg">
        Contact
      </h2>
      <div class="formGroup">
        <label class="formGroup__label" for="name">Your Name</label>
        <input class="formGroup__input" type="text" placeholder="Taro Yamada" v-model="contactForm.name" />
      </div>
      <div class="formGroup">
        <label class="formGroup__label" for="name">Comment</label>
        <textarea class="formGroup__textArea" placeholder="comment" v-model="contactForm.comment" />
      </div>
      <button class="formButton" @click="submitForm">
        <div>Submit Form</div>
        <img class="section__title__icon" src="/images/icon/paper-plane.svg">
      </button>
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