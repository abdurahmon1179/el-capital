<template>
  <Container class="py-[80px] px-[40px] sm:py-[100px] lg:py-[120px] flex flex-col lg:flex-row gap-10 lg:gap-[80px]">
    <div class="flex-1">
      <h2 class="font-semibold text-[28px] sm:text-[32px] md:text-[36px] pb-8 sm:pb-12 lg:pb-[80px]">Контактлар</h2>
      
      <div class="mb-8 sm:mb-12">
        <div class="flex items-center gap-3 sm:gap-[14px] mb-2 sm:mb-4">
          <img src="/img/loc.svg" alt="location">
          <p class="text-[16px] sm:text-[18px] font-medium">Манзил:</p>
        </div>
        <p class="font-semibold text-[16px] sm:text-[18px] md:text-[20px]">
          100015, Ўзбекистон Республикаси, Тошкент шаҳри, Миробод тумани, Нукус кўчаси, 22-уй
        </p>
      </div>

      <div class="flex flex-col sm:flex-row sm:gap-8 lg:gap-[200px] mb-8 sm:mb-12">
        <div class="mb-6 sm:mb-0">
          <div class="flex items-center gap-3 sm:gap-[14px] mb-2 sm:mb-4">
            <img src="/img/call.svg" alt="phone">
            <p class="text-[16px] sm:text-[18px] font-medium">Телефон ракам:</p>
          </div>
          <p class="font-semibold text-[16px] sm:text-[18px] md:text-[20px]">+998 91 125 45 67</p>
        </div>

        <div>
          <div class="flex items-center gap-3 sm:gap-[14px] mb-2 sm:mb-4">
            <img src="/img/email.svg" alt="email">
            <p class="text-[16px] sm:text-[18px] font-medium">Электрон почта:</p>
          </div>
          <p class="font-semibold text-[16px] sm:text-[18px] md:text-[20px]">info@example.com</p>
        </div>
      </div>

      <div>
        <div class="flex items-center gap-3 sm:gap-[14px] mb-2 sm:mb-4">
          <img src="/img/email.svg" alt="working hours">
          <p class="text-[16px] sm:text-[18px] font-medium">Иш вакти:</p>
        </div>
        <p class="font-semibold text-[16px] sm:text-[18px] md:text-[20px]">
          Душанба–Жума 09:00 – 18:00 <br> Шанба–Якшанба дам олиш кунлари
        </p>
      </div>
    </div>

    <div class="flex-1 w-full">
      <div class="relative w-full pt-[56.25%] sm:pt-[60%] lg:pt-[56.25%]">
        <iframe
          class="absolute top-0 left-0 w-full h-full rounded-xl shadow-lg border-0"
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
