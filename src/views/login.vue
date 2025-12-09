<template>
    <div class="h-screen flex items-center justify-center background-logo px-4 relative">
 
        <transition name="fade">
            <button v-show="showForm" @click="closeForm"
                class="absolute top-8 left-8 text-[#002B5B] text-2xl flex items-center gap-2 z-50">
                <i class="bi bi-arrow-left"></i>
                Орқага
            </button>
        </transition>

        <transition name="fade">
            <div v-if="showForm"
                class="absolute  inset-0 flex items-center justify-center bg-[#F6F6F6] background-logo bg-opacity-95 px-4">
                <div class="w-full max-w-[575px] py-[34px] px-[28px] bg-white rounded-[28px] shadow-lg">

                    <form @submit.prevent="login" class="flex flex-col gap-[18px] w-full">
                        <input
                            v-model.trim="email"
                            class="bg-[#EAEFEF33] border border-[#CACACA4D] py-[19.5px] pl-[24px] w-full rounded-[12px]"
                            placeholder="Login" type="email">

                        <input
                            v-model.trim="password"
                            class="bg-[#EAEFEF33] border border-[#CACACA4D] py-[19.5px] pl-[24px] w-full rounded-[12px]"
                            placeholder="Парол" type="password">
                    
                        <button
                            class=" mt-[20px] w-full bg-[#002B5B] h-[64px] sm:h-[64px] rounded-[12px] text-white mb-[14px]">
                            Кириш
                        </button>
                    </form>

                </div>
            </div>
        </transition>

        <div v-if="!showForm" class="w-full max-w-[575px] py-[34px] px-[28px] bg-white rounded-[28px]">
            <h2 class="text-center font-medium text-[32px] sm:text-[38px] mb-[14px]">
                Тизимга кириш
            </h2>

            <p class="text-[#727272] text-[18px] sm:text-[24px] leading-[145%] text-center mb-[40px] sm:mb-[54px] px-2">
                Тизимга кириш учун шахсий логин ва паролни киритинг
            </p>

            <div class="w-full pb-[40px] sm:pb-[52px]">
                <button @click="showForm = true"
                    class="w-full bg-[#002B5B] h-[56px] sm:h-[64px] rounded-[12px] text-white mb-[14px]">
                    Кириш
                </button>
                <button class="w-full bg-[#E7EAEE] h-[56px] sm:h-[64px] rounded-[12px] block">
                    ЕРИ калит
                </button>
            </div>

            <p class="text-center text-sm sm:text-base px-4">
                Илтимос, хизмат кўрсатиш сифати ва тажрибангизни шахсийлаштириш учун маълумотларингизни қайта ишлашга
                рухсат беринг.
            </p>
        </div>

    </div>
</template>

<script setup>
import { ref } from 'vue'
import { useRouter } from 'vue-router'
import { toast } from "vue3-toastify"
import "vue3-toastify/dist/index.css"

const router = useRouter()

const showForm = ref(false)
const email = ref("")
const password = ref("")

function closeForm() {
    showForm.value = false
}

function login() {
    if (!email.value || !password.value) {
        toast.error("Илтимос, барча майдонларни тўлдиринг", { autoClose: 2500 })
        return
    }

 
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/

    if (!emailRegex.test(email.value)) {
        toast.error("Илтимос, тўғри email киритинг!", { autoClose: 2500 })
        return
    }

    toast.success("Муваффақиятли кирдингиз!", { autoClose: 2000 })
    router.push("/")
}

</script>

<style scoped>
.background-logo {
    background-image: url(/img/back.svg);
    background-repeat: no-repeat;
    background-position: center center;
    background-size: 100% 100%;
}

.fade-enter-active,
.fade-leave-active {
    transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}

@media (min-width: 1024px) {
    .background-logo {
        background-size: 700px auto;
    }
}
</style>
