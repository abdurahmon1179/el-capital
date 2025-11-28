<template>
    <footer class="bg-[#003366] text-white py-12 mt-20">
        <Container>
            <div class="flex gap-[200px]">
                <div class="flex flex-col justify-between w-50">
                    <div class="flex gap-[70px]">
                        <img src="/img/footer-logo.svg" alt="" class="h-[50px]">
                        <img src="/img/logo2.svg" alt="" class="h-[50px]">
                    </div>
                    <p class="text-sm opacity-70">2025 © REALSOFT Барча ҳуқуқлар ҳимояланган</p>
                </div>

                <div class="flex justify-between w-300">
                    <div class="space-y-4">
                        <h3 class="font-semibold text-lg text-[#FFFFFF80]">Бўлимлар</h3>
                        <ul class="space-y-2 opacity-80">
                            <li>Бош саҳифа</li>
                            <li>Меъёрий ҳужжатлар</li>
                            <li>Қўлланма</li>
                            <li>Реестр</li>
                            <li>Боғланиш</li>
                        </ul>
                    </div>

                    <div class="space-y-4">
                        <h3 class="font-semibold text-lg text-[#FFFFFF80]">Бўлимлар</h3>
                        <ul class="space-y-2 opacity-80">
                            <li>(+99871) 231-79-09</li>
                            <li>info@napp.uz</li>
                            <li>Душанба–Жума 09:00 – 18:00</li>
                            <li>Шанба–Якшанба дам олиш кунлари</li>
                            <li class="w-[400px]">
                                100015, Ўзбекистон Республикаси, Тошкент шаҳри,
                                Миробод тумани, Нукус кўчаси, 22-уй
                            </li>
                        </ul>
                    </div>

                    <div class="space-y-4">
                        <h3 class="font-semibold text-lg text-[#FFFFFF80]">Ижтимоий тармоқлар</h3>
                        <ul class="space-y-2 opacity-80">
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
