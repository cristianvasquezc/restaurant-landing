<script setup lang="ts">
import BaseLayout from '@/layouts/BaseLayout.vue';
import { RouterLink } from 'vue-router';

</script>

<template>
    <BaseLayout>
        <section class="h-[calc(100vh-80px)] flex flex-col items-center justify-center bg-primary text-white">
            <h1 class="text-7xl font-bold">404</h1>
            <n-p>Page not found</n-p>

            <RouterLink :to="{ name: 'home' }">
                <n-button round color="white" text-color="black">
                    Go back home
                </n-button>
            </RouterLink>
        </section>
    </BaseLayout>
</template>
