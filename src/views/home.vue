<script setup>
import Header from "../components/header/index.vue"
import Hero from "../components/hero/index.vue"
import Service from "../components/service/index.vue"
import Calendar from "../components/calendar/index.vue"
import Question from "../components/question/index.vue"
import News from "../components/news/index.vue"
import Contact from "../components/contact/index.vue"
import Footer from "../components/footer/index.vue"
</script>

<template>
  <div class="header">
    <Header />
    <Hero />
  </div>
  <Service />
  <Calendar />
  <Question />
  <News />
  <Contact />
  <Footer />
</template>
