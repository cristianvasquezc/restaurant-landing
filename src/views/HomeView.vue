<script setup lang="ts">
import HeroSection from '@/components/section/HeroSection.vue';
import WelcomeSection from '@/components/section/WelcomeSection.vue';
import WhereFindUsSection from '@/components/section/WhereFindUsSection.vue';
import BaseLayout from '@/layouts/BaseLayout.vue';


</script>

<template>
    <BaseLayout>
        <HeroSection />

        <WelcomeSection />

        <WhereFindUsSection />
    </BaseLayout>
</template>
