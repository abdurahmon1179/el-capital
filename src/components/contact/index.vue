<template>
    <Container class="py-[120px] flex gap-[80px]">
        <div>
            <div>
                <h2 class="font-semibold text-[36px] pb-[80px]">Контактлар</h2>
                <div class="mb-[50px]">
                    <div class="flex items-center gap-[14px] mb-[14px]">
                        <img src="../../../public/img/loc.svg" alt="">
                        <p>Манзил:</p>
                    </div>
                    <p class="font-semibold text-[20px]">100015, Ўзбекистон Республикаси, Тошкент шаҳри, Миробод тумани,
                        Нукус кўчаси, 22-уй</p>
                </div>
                <div class="flex gap-[200px]">
                    <div class="mb-[50px]">
                        <div class="flex items-center gap-[14px] mb-[14px]">
                            <img src="../../../public/img/call.svg" alt="">
                            <p>Телефон ракам:</p>
                        </div>
                        <p class="font-semibold text-[20px]">+998 91 125 45 67</p>
                    </div>

                    <div class="mb-[50px]">
                        <div class="flex items-center gap-[14px] mb-[14px]">
                            <img src="../../../public/img/email.svg" alt="">
                            <p>Электрон почта:</p>
                        </div>
                        <p class="font-semibold text-[20px]">+998 91 125 45 67</p>
                    </div>
                </div>
                <div>
                    <div class="flex items-center gap-[14px] mb-[14px]">
                        <img src="../../../public/img/email.svg" alt="">
                        <p>Иш вакти:</p>
                    </div>
                    <p class="font-semibold text-[20px]">Душанба–Жума 09:00 – 18:00
                        Шанба–Якшанба дам олиш кунлари</p>
                </div>
            </div>
        </div>
        <img src="../../../public/img/map.svg" alt="">
    </Container>
</template>

<script setup>
import Container from "../layouts/index.vue"
</script>