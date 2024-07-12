<script setup>
import { Head, Link } from '@inertiajs/vue3';

import TwitterLayout from "@/Layouts/TwitterLayout.vue";
</script>

<template>
    <Head title="Анонимная соцсеть" />
    <TwitterLayout>
        <div class="text-white">
            <Tweet :tweet="{
                id: 1,
                text: 'Тестовая запись',
                user: {
                    name: 'Аноним',
                    avatar: 'https://i.imgur.com/0333333.png'
                },
                created_at: '2021-09-20 12:00:00',
                likes: 10,
                comments: 1
            }"/>
            <div class="border-b border-b-gray-800 mt-2"></div>
        </div>
    </TwitterLayout>
</template>
