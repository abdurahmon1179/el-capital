<template>
    <Container class="text-white flex items-center justify-between pt-[70px] pb-[50px] xl:pb-[120px] px-[40px] relative z-50">

        <div class="flex items-center gap-[30px] sm:gap-[60px]">
            <img class="w-[55px] h-[60px] sm:w-auto sm:h-auto" src="/public/img/logo.svg" alt="">
            <img class="w-[200px] h-[50px] sm:w-auto sm:h-auto" src="/public/img/logo2.svg" alt="">
        </div>

        <div class="gap-[40px] hidden xl:flex">
            <ul class="flex gap-[20px]">
                <li class="cursor-pointer">Календарь</li>
                <li class="cursor-pointer">Документы</li>
                <li class="cursor-pointer">Новости</li>
                <li class="cursor-pointer">Реестр</li>
                <li class="cursor-pointer">Контакты</li>
            </ul>

            <div class="flex gap-[20px]">
                <p>День/Ночь</p>
                <p>Ру</p>
            </div>

            <router-link to="/login" class="cursor-pointer">
                Вход в систему
            </router-link>
        </div>

        <button @click="open = !open"
            class="relative w-10 h-10 flex items-center justify-center xl:hidden focus:outline-none">

            <span class="block absolute w-6 h-[2px] rounded bg-white transition-all duration-300"
                :class="open ? 'opacity-0' : 'opacity-100'"></span>

            <span class="block absolute w-6 h-[2px] rounded bg-white transition-all duration-300"
                :class="open ? 'rotate-45' : '-translate-y-2.5'"></span>

            <span class="block absolute w-6 h-[2px] rounded bg-white transition-all duration-300"
                :class="open ? '-rotate-45' : 'translate-y-2.5'"></span>
        </button>
    </Container>


    <div
        :class="open ? 'translate-x-0' : '-translate-x-full'"
        class="fixed top-0 left-0 w-full h-full bg-[#0e0e0e] text-white p-8 flex justify-center items-center text-center flex-col gap-8 transition-transform duration-300 xl:hidden z-40">


        <ul class="flex flex-col gap-6 text-[22px] mt-[100px]">
            <li class="cursor-pointer">Календарь</li>
            <li class="cursor-pointer">Документы</li>
            <li class="cursor-pointer">Новости</li>
            <li class="cursor-pointer">Реестр</li>
            <li class="cursor-pointer">Контакты</li>
        </ul>

        <div class="flex gap-[20px] text-[20px]">
            <p>День/Ночь</p>
            <p>Ру</p>
        </div>

        <router-link to="/login" class="cursor-pointer text-[20px]">
            Вход в систему
        </router-link>
    </div>

</template>




<script setup>
import Container from "../layouts/index.vue"
import { ref } from 'vue'



const open = ref(false)
</script>