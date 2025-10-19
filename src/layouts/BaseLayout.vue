<script setup lang="ts">
import Footer from '@/components/layout/Footer.vue';
import Navbar from '@/components/layout/Navbar.vue';

</script>

<template>
    <div>
        <Navbar />
        <main class="w-full px-2">
            <slot />
        </main>
        <Footer />
    </div>
</template>
