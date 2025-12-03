<template>
  <Container class="py-[120px] px-4 md:px-[40px]">
    <h1 class="text-[28px] md:text-[36px] font-semibold pb-[20px]">Савол-жавоблар</h1>
    <p class="text-[18px] md:text-[24px] w-full md:w-[750px] leading-[135%] pb-[60px]">
      Капитал бозори ҳақида кўп сўраладиган саволлар ва уларга содда жавоблар шу ерда жамланган.
    </p>

    <div class="w-full md:w-full">
      <div v-for="(item, index) in accordions" :key="index" class="mb-6 md:mb-[24px]">
        <div
          class="flex items-center justify-between mb-[20px] cursor-pointer"
          @click="toggle(index)"
        >
          <h2 class="font-semibold text-[16px] sm:text-[18px] md:text-[22px] flex-1 truncate pr-4 leading-[120%]">
            {{ item.title }}
          </h2>
          <img
            class="w-6 h-6 md:w-6 md:h-6 flex-shrink-0"
            :src="item.isOpen ? minusImg : plusImg"
            alt=""
          >
        </div>

        <transition
          enter-active-class="transition-all duration-300 ease-out"
          leave-active-class="transition-all duration-200 ease-in"
          enter-from-class="max-h-0 opacity-0"
          enter-to-class="max-h-96 opacity-100"
          leave-from-class="max-h-96 opacity-100"
          leave-to-class="max-h-0 opacity-0"
        >
          <p v-if="item.isOpen" class="overflow-hidden pb-4 md:pb-[24px] text-[14px] sm:text-[16px] md:text-[18px]">
            {{ item.text }}
          </p>
        </transition>

        <hr class="border-gray-300">
      </div>
    </div>
  </Container>
</template>

<script setup>
import Container from "../layouts/index.vue"
import { ref } from 'vue'

import plusImg from "/img/plus.svg"
import minusImg from '/img/minus.svg'

const accordions = ref([
  {
    title: "Қимматли қоғозлар чиқарилишини давлат рўйхатидан ўтказиш модули (ҚҚЧДРУМ) нима ?",
    text: "ҚҚЧДРУМ — бу Ўзбекистон Республикаси қонунчилигига мувофиқ қимматли қоғозларни давлат рўйхатидан ўтказиш ва бекор қилиш жараёнларини автоматлаштиришга мўлжалланган махсус ахборот тизимидир.",
    isOpen: false
  },
  {
    title: "Қимматли қоғозлар чиқарилишини давлат рўйхатидан ўтказиш модули (ҚҚЧДРУМ) нима ?",
    text: "ҚҚЧДРУМ — бу Ўзбекистон Республикаси қонунчилигига мувофиқ қимматли қоғозларни давлат рўйхатидан ўтказиш ва бекор қилиш жараёнларини автоматлаштиришга мўлжалланган махсус ахборот тизимидир.",
    isOpen: false
  },
  {
    title: "Қимматли қоғозлар чиқарилишини давлат рўйхатидан ўтказиш модули (ҚҚЧДРУМ) нима ?",
    text: "ҚҚЧДРУМ — бу Ўзбекистон Республикаси қонунчилигига мувофиқ қимматли қоғозларни давлат рўйхатидан ўтказиш ва бекор қилиш жараёнларини автоматлаштиришга мўлжалланган махсус ахборот тизимидир.",
    isOpen: false
  },
  {
    title: "Қимматли қоғозлар чиқарилишини давлат рўйхатидан ўтказиш модули (ҚҚЧДРУМ) нима ?",
    text: "ҚҚЧДРУМ — бу Ўзбекистон Республикаси қонунчилигига мувофиқ қимматли қоғозларни давлат рўйхатидан ўтказиш ва бекор қилиш жараёнларини автоматлаштиришга мўлжалланган махсус ахборот тизимидир.",
    isOpen: false
  },
  {
    title: "Қимматли қоғозлар чиқарилишини давлат рўйхатидан ўтказиш модули (ҚҚЧДРУМ) нима ?",
    text: "ҚҚЧДРУМ — бу Ўзбекистон Республикаси қонунчилигига мувофиқ қимматли қоғозларни давлат рўйхатидан ўтказиш ва бекор қилиш жараёнларини автоматлаштиришга мўлжалланган махсус ахборот тизимидир.",
    isOpen: false
  },
])

function toggle(index) {
  accordions.value[index].isOpen = !accordions.value[index].isOpen
}
</script>
