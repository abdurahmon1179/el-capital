<template>
  <footer class="bg-[#003366] text-white py-12 mt-20">
    <Container class="px-[40px]">
      <div class="flex flex-col lg:flex-row gap-10 lg:gap-[200px] text-center lg:text-left">
        <!-- Logo va huquqlar -->
        <div class="flex flex-col justify-between items-center lg:items-start">
  <div class="flex gap-4 sm:gap-8 mb-4 lg:mb-0">
    <img src="/img/footer-logo.svg" alt="" class="h-10 sm:h-[50px]">
    <img src="/img/logo2.svg" alt="" class="h-10 sm:h-[50px]">
  </div>
  <p class="text-sm sm:text-base opacity-70 text-center lg:text-left">
    2025 © REALSOFT Барча ҳуқуқлар ҳимояланган
  </p>
</div>


        <!-- Menular -->
        <div class="flex flex-col sm:flex-row justify-between gap-8 sm:gap-12 lg:gap-[100px]">
          <!-- Bo‘limlar 1 -->
          <div class="space-y-3 sm:space-y-4">
            <h3 class="font-semibold text-base sm:text-lg text-[#FFFFFF80]">Бўлимлар</h3>
            <ul class="space-y-1 sm:space-y-2 opacity-80">
              <li>Бош саҳифа</li>
              <li>Меъёрий ҳужжатлар</li>
              <li>Қўлланма</li>
              <li>Реестр</li>
              <li>Боғланиш</li>
            </ul>
          </div>

          <!-- Bo‘limlar 2 (Kontaktlar) -->
          <div class="space-y-3 sm:space-y-4">
            <h3 class="font-semibold text-base sm:text-lg text-[#FFFFFF80]">Контактлар</h3>
            <ul class="space-y-1 sm:space-y-2 opacity-80">
              <li>(+99871) 231-79-09</li>
              <li>info@napp.uz</li>
              <li>Душанба–Жума 09:00 – 18:00</li>
              <li>Шанба–Якшанба дам олиш кунлари</li>
              <li class="sm:w-[300px] lg:w-[400px] text-sm sm:text-base">
                100015, Ўзбекистон Республикаси, Тошкент шаҳри,
                Миробод тумани, Нукус кўчаси, 22-уй
              </li>
            </ul>
          </div>

          <!-- Ijtimoiy tarmoqlar -->
          <div class="space-y-3 sm:space-y-4">
            <h3 class="font-semibold text-base sm:text-lg text-[#FFFFFF80]">Ижтимоий тармоқлар</h3>
            <ul class="space-y-1 sm:space-y-2 opacity-80">
              <li>Twitter</li>
              <li>Telegram</li>
              <li>Instagram</li>
              <li>Facebook</li>
              <li>YouTube</li>
            </ul>
          </div>
        </div>
      </div>
    </Container>
  </footer>
</template>

<script setup>
import Container from "../layouts/index.vue"
</script>
