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
  v-model="email"
  class="bg-[#EAEFEF33] border border-[#CACACA4D] py-[19.5px] pl-[24px] w-full rounded-[12px]"
  placeholder="Login"
  type="email"
/>
<p v-if="emailError" class="text-red-500 text-sm">
  {{ emailError }}
</p>


 <input
  v-model="password"
  class="bg-[#EAEFEF33] border border-[#CACACA4D] py-[19.5px] pl-[24px] w-full rounded-[12px]"
  placeholder="Парол"
  type="password"
/>
<p v-if="passwordError" class="text-red-500 text-sm">
  {{ passwordError }}
</p>

                    
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
import { ref } from "vue"
import { useRouter } from "vue-router"
import { toast } from "vue3-toastify"
import "vue3-toastify/dist/index.css"
import { useForm, useField } from "vee-validate"
import * as yup from "yup"

const router = useRouter()
const showForm = ref(false)

const schema = yup.object({
  email: yup
    .string()
    .required("Email мажбурий")
    .email("Тўғри email киритинг"),
  password: yup
    .string()
    .required("Парол мажбурий")
    .min(6, "Парол камида 6 та белги бўлсин")
})

const { handleSubmit } = useForm({
  validationSchema: schema
})

const { value: email, errorMessage: emailError } = useField("email")
const { value: password, errorMessage: passwordError } = useField("password")

const login = handleSubmit(() => {
  toast.success("Муваффақиятли кирдингиз!", { autoClose: 2000 })
  router.push("/")
})

function closeForm() {
  showForm.value = false
}
</script>


<style scoped>
.background-logo {
    background-image: url(/img/back.svg);
    background-repeat: no-repeat;
    background-position: center center;
    background-size: 100% 100%;
    font-family: Inter;
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
