<template>
  <Container class="py-[120px]">
    <h1 class="text-[36px] font-semibold pb-[20px]">Савол-жавоблар</h1>
    <p class="text-[24px] w-[750px] leading-[135%] pb-[80px]">
      Капитал бозори ҳақида кўп сўраладиган саволлар ва уларга содда жавоблар шу ерда жамланган.
    </p>

    <div class="w-[995px]">
      <div v-for="(item, index) in accordions" :key="index" class="mb-[24px]">
        <div class="flex items-center justify-between mb-[20px]">
          <h2 class="font-semibold text-[22px] w-[700px] leading-[120%]">
            {{ item.title }}
          </h2>
          <img
            class="cursor-pointer"
            :src="item.isOpen ? minusImg : plusImg"
            alt=""
            @click="toggle(index)"
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
          <p v-if="item.isOpen" class="overflow-hidden pb-[24px]">
            {{ item.text }}
          </p>
        </transition>

        <hr>
      </div>
    </div>
  </Container>
</template>

<script setup>
import Container from "../layouts/index.vue"
import { ref } from 'vue'

import plusImg from "../../../public/img/plus.svg"
import minusImg from '../../../public/img/minus.svg'


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
