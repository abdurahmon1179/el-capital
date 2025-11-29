<template>
  <Container class="py-[120px] flex flex-col lg:flex-row gap-[80px]">
    <!-- Kontaktlar -->
    <div class="flex-1">
      <h2 class="font-semibold text-[36px] pb-[80px]">Контактлар</h2>
      
      <div class="mb-[50px]">
        <div class="flex items-center gap-[14px] mb-[14px]">
          <img src="/img/loc.svg" alt="">
          <p>Манзил:</p>
        </div>
        <p class="font-semibold text-[20px]">100015, Ўзбекистон Республикаси, Тошкент шаҳри, Миробод тумани, Нукус кўчаси, 22-уй</p>
      </div>

      <div class="flex flex-col lg:flex-row lg:gap-[200px] mb-[50px]">
        <div class="mb-[50px]">
          <div class="flex items-center gap-[14px] mb-[14px]">
            <img src="/img/call.svg" alt="">
            <p>Телефон ракам:</p>
          </div>
          <p class="font-semibold text-[20px]">+998 91 125 45 67</p>
        </div>

        <div class="mb-[50px]">
          <div class="flex items-center gap-[14px] mb-[14px]">
            <img src="/img/email.svg" alt="">
            <p>Электрон почта:</p>
          </div>
          <p class="font-semibold text-[20px]">info@example.com</p>
        </div>
      </div>

      <div>
        <div class="flex items-center gap-[14px] mb-[14px]">
          <img src="/img/email.svg" alt="">
          <p>Иш вакти:</p>
        </div>
        <p class="font-semibold text-[20px]">Душанба–Жума 09:00 – 18:00 <br> Шанба–Якшанба дам олиш кунлари</p>
      </div>
    </div>

    <div class="flex-1">
      <div class="relative w-full" style="padding-top: 56.25%;"> 
        <iframe
          class="absolute top-0 left-0 w-full h-[700px] rounded-xl shadow-lg border-0"
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2847.675202292171!2d69.2872347758757!3d41.33256277130687!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38ae8bc81d43da97%3A0xa44255ba2a280e29!2sRealSoft!5e1!3m2!1sru!2s!4v1764349806135!5m2!1sru!2s"
          allowfullscreen
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade">
        </iframe>
      </div>
    </div>
  </Container>
</template>

<script setup>
import Container from "../layouts/index.vue"
</script>
