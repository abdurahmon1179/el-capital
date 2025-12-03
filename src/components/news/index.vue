<template>
  <section class="bg-[#002B5B0D] py-[120px]">
    <Container class="px-[40px]">
      <h1 class="text-[28px] sm:text-[32px] md:text-[36px] font-semibold pb-[20px]">
        Сўнгги янгиликлар
      </h1>
      <p class="text-[16px] sm:text-[18px] md:text-[24px] leading-[135%] w-full md:w-[900px] pb-[60px]">
        Капитал бозоридаги сўнгги янгиликлар, қонунчиликдаги ўзгаришлар ва инвестиция имкониятлари ҳақида қисқа ва ишончли маълумотлар жамланади.
      </p>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8">
        <div
          v-for="(news, index) in newsList"
          :key="index"
          class="bg-white p-4 sm:p-6 rounded-[18px] flex flex-col"
        >
          <img class="mb-4 sm:mb-6 w-full h-auto rounded-[12px]" :src="news.img" :alt="news.title" />
          <h2 class="font-bold text-[18px] sm:text-[20px] md:text-[22px] leading-[135%] mb-2">
            {{ news.title }}
          </h2>
          <p class="text-[#00000080] text-[14px] sm:text-[16px] md:text-[18px] leading-[145%] mb-4">
            {{ news.desc }}
          </p>
          <p class="font-medium text-[14px] sm:text-[16px] text-right text-gray-600">
            {{ news.date }}
          </p>
        </div>
      </div>
    </Container>
  </section>
</template>

<script setup>
import Container from "../layouts/index.vue"

const newsList = [
  {
    img: "/img/new.svg",
    title: "Агентлик делегациясининг фонд бозори тажрибасини ўрганиш мақсадида Корея",
    desc: "Истиқболли лойиҳалар миллий агентлиги (агентлик) вакилларининг Корея Республикаси фонд",
    date: "10 04 2025"
  },
  {
    img: "/img/new.svg",
    title: "Агентлик делегациясининг фонд бозори тажрибасини ўрганиш мақсадида Корея",
    desc: "Истиқболли лойиҳалар миллий агентлиги (агентлик) вакилларининг Корея Республикаси фонд",
    date: "10 04 2025"
  },
  {
    img: "/img/new.svg",
    title: "Агентлик делегациясининг фонд бозори тажрибасини ўрганиш мақсадида Корея",
    desc: "Истиқболли лойиҳалар миллий агентлиги (агентлик) вакилларининг Корея Республикаси фонд",
    date: "10 04 2025"
  },
  {
    img: "/img/new.svg",
    title: "Агентлик делегациясининг фонд бозори тажрибасини ўрганиш мақсадида Корея",
    desc: "Истиқболли лойиҳалар миллий агентлиги (агентлик) вакилларининг Корея Республикаси фонд",
    date: "10 04 2025"
  },
  {
    img: "/img/new.svg",
    title: "Агентлик делегациясининг фонд бозори тажрибасини ўрганиш мақсадида Корея",
    desc: "Истиқболли лойиҳалар миллий агентлиги (агентлик) вакилларининг Корея Республикаси фонд",
    date: "10 04 2025"
  },
  {
    img: "/img/new.svg",
    title: "Агентлик делегациясининг фонд бозори тажрибасини ўрганиш мақсадида Корея",
    desc: "Истиқболли лойиҳалар миллий агентлиги (агентлик) вакилларининг Корея Республикаси фонд",
    date: "10 04 2025"
  },
]
</script>
