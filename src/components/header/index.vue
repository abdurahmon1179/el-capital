<template>
    <Container class="text-white flex items-center justify-between pt-[70px] pb-[120px]">
        <div class="flex items-center gap-[60px]">
            <img src="/public/img/logo.svg" alt="">
            <img src="/public/img/logo2.svg" alt="">
        </div>
        <div class="flex gap-[40px]">
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
            <router-link to="/login" class="cursor-pointer">Вход в систему</router-link>
        </div>
    </Container>
</template>

<script setup>
import Container from "../layouts/index.vue"
</script>