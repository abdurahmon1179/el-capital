<template>
  <section class="bg-[#002B5B0D] py-[120px]">
    <Container class="px-[40px]">
      <h1 class="font-semibold text-[36px] mb-[20px]">Календарь</h1>

      <!-- Buttons -->
      <div class="flex flex-wrap gap-4 mb-[80px]">
        <div class="flex gap-2 flex-wrap">
          <button
            v-for="(btn, index) in group1"
            :key="index"
            @click="active1 = index"
            :class="[
              'py-2 px-6 rounded-full cursor-pointer font-medium transition',
              active1 === index ? 'bg-[#002B5B] text-white' : 'bg-white text-black'
            ]"
          >
            {{ btn }}
          </button>
        </div>
        <div class="flex gap-2 flex-wrap">
          <button
            v-for="(btn, index) in group2"
            :key="index"
            @click="active2 = index"
            :class="[
              'py-2 px-6 rounded-full cursor-pointer font-medium transition',
              active2 === index ? 'bg-[#002B5B] text-white' : 'bg-white text-black'
            ]"
          >
            {{ btn }}
          </button>
        </div>
      </div>

      <!-- Responsive Table -->
      <div class="overflow-x-auto rounded-[12px] border border-[#0000001A]">
        <table class="w-full min-w-[700px] border-collapse">
          <thead>
            <tr class="bg-[#002B5B] text-white text-left">
              <th class="py-4 px-5 font-semibold">Эмитент номи</th>
              <th class="py-4 px-5 font-semibold">Қарор санаси</th>
              <th class="py-4 px-5 font-semibold">Суммаси (UZS)</th>
              <th class="py-4 px-5 font-semibold">Фоиз (%)</th>
              <th class="py-4 px-5 font-semibold">Бошланиш санаси</th>
              <th class="py-4 px-5 font-semibold">Туғаш санаси</th>
            </tr>
          </thead>

          <tbody>
            <tr
              v-for="(item, index) in tableData"
              :key="index"
              class="border-b border-[#0000000D] hover:bg-[#F7F9FB]"
            >
              <td class="py-3 px-5 text-[15px] text-[#002B5B] whitespace-nowrap">
                {{ item.name }}
              </td>
              <td class="py-3 px-5 whitespace-nowrap">{{ item.decisionDate }}</td>
              <td class="py-3 px-5 whitespace-nowrap">{{ item.amount }}</td>
              <td class="py-3 px-5 whitespace-nowrap">{{ item.percent }}</td>
              <td class="py-3 px-5 whitespace-nowrap">{{ item.startDate }}</td>
              <td class="py-3 px-5 whitespace-nowrap">{{ item.endDate }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </Container>
  </section>
</template>

<script setup>
import { ref } from "vue"
import Container from "../layouts/index.vue"

const group1 = ["Дивидентлар", "Эълонлар", "Хисобот"]
const group2 = ["Оддий акциялар", "Имтийозли акциялар", "Облигациялар"]

const active1 = ref(0)
const active2 = ref(0)

const tableData = [
  { name: "Biznes Finans Mikromoliya Tashkiloti", decisionDate: "2023-08-16", amount: "2 219,18", percent: "2.22", startDate: "2025-07-22", endDate: "2025-08-04" },
  { name: "IMKON FINANS mikromoliya tashkiloti AJ", decisionDate: "2024-01-31", amount: "23 013,7", percent: "2.3", startDate: "2025-07-18", endDate: "2025-07-27" },
  { name: "O‘zIQMK AJ", decisionDate: "2024-06-11", amount: "94 739,73", percent: "9.47", startDate: "2025-07-08", endDate: "2025-07-10" },
  { name: "AGAT CREDIT AJ MMT", decisionDate: "2025-01-16", amount: "2 383,56", percent: "2.38", startDate: "2025-06-02", endDate: "2025-07-01" },
  { name: "Biznes Finans Mikromoliya Tashkiloti", decisionDate: "2024-11-18", amount: "2 219,18", percent: "2.22", startDate: "2025-07-04", endDate: "2025-07-17" },
  { name: "Biznes Finans Mikromoliya Tashkiloti", decisionDate: "2022-07-25", amount: "22 191,78", percent: "2.22", startDate: "2025-07-02", endDate: "2025-07-15" },
  { name: "DELTA MIKROMOLIYA TASHKILOTI MChJ", decisionDate: "2025-01-29", amount: "23 013,69", percent: "2.3", startDate: "2025-06-25", endDate: "2025-07-05" },
  { name: "IMKON FINANS mikromoliya tashkiloti AJ", decisionDate: "2022-06-30", amount: "23 013,7", percent: "2.3", startDate: "Invalid date", endDate: "2025-06-25" },
  { name: "Biznes Finans Mikromoliya Tashkiloti", decisionDate: "2023-08-16", amount: "2 219,18", percent: "2.22", startDate: "2025-06-23", endDate: "2025-07-08" },
  { name: "O‘zIQMK AJ", decisionDate: "2025-02-15", amount: "44 876,71", percent: "4.49", startDate: "2025-06-19", endDate: "2025-06-23" }
]
</script>