<template>
    <div class="rounded-full w-full lg:inline-block hover:bg-gray-900 p-2 px-4 lg:pr-6 cursor-pointer transition duration-200 ease-in-out">        <div class="flex items-center">
            <component :is="icon" fillColor="#FFFFFF" size="30"/>
            <span class="lg:block hidden text-white font-bold text-[23px] pl-4 mt-0.5">
                {{ iconString }}
            </span>
        </div>
    </div>
</template>

<script setup>
import {toRefs } from 'vue'
import Home from 'vue-material-design-icons/Home.vue';
import Pound from 'vue-material-design-icons/Pound.vue';
import BellOutline from 'vue-material-design-icons/BellOutline.vue';
import EmailOutline from 'vue-material-design-icons/EmailOutline.vue';
import AccountOutline from 'vue-material-design-icons/AccountOutline.vue';
const props = defineProps({
    iconString: String,
})

const { iconString } = toRefs(props)

let icon = null
if (iconString.value === 'Главная') icon = Home
if (iconString.value === 'Новости') icon = Pound
if (iconString.value === 'Уведомления') icon = BellOutline
if (iconString.value === 'Сообщения') icon = EmailOutline
if (iconString.value === 'Профиль') icon = AccountOutline



</script>
