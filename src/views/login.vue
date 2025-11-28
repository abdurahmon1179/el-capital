<template>
    <div class="flex h-screen justify-between background-logo">
        <div class="pt-[10px] ml-[100px]">
            <div class="w-[575px] py-[34px] px-[28px] bg-white rounded-[28px]">
                <h2 class="text-center font-medium text-[38px] mb-[14px]">Тизимга кириш</h2>
                <p class="text-[#727272] text-[24px] leading-[145%] w-[520px] text-center mb-[54px]">
                    Тизимга кириш учун шахсий логин ва паролни киритинг
                </p>
                <form class="flex flex-col gap-[18px] mb-[34px] w-full">
                    <input class="bg-[#EAEFEF33] border border-[#CACACA4D] py-[19.5px] pl-[24px] w-full rounded-[12px]" placeholder="Login" type="email">
                    <input class="bg-[#EAEFEF33] border border-[#CACACA4D] py-[19.5px] pl-[24px] w-full rounded-[12px]" placeholder="Парол" type="password">
                </form>
                <div class="w-full pb-[52px]">
                    <button class="w-full bg-[#002B5B] h-[64px] rounded-[12px] text-white mb-[14px]">Кириш</button>
                    <button class="w-full bg-[#E7EAEE] h-[64px] rounded-[12px] block">ЕРИ калит</button>
                </div>
                <p class="text-center">
                    Илтимос, хизмат кўрсатиш сифати ва тажрибангизни шахсийлаштириш учун маълумотларингизни қайта ишлашга рухсат беринг.
                </p>
            </div>
        </div>

        <div>
            <img class="login" src="../../../public/img/login.svg" alt="">
        </div>
    </div>
</template>


<style scoped>
.background-logo {
    background-image: url(/img/back.svg);
    background-repeat: no-repeat;
    background-position: left center;
    margin-left: 50px;
}

.login {
    height: 100vh;
    /* width: auto; */
}



</style>