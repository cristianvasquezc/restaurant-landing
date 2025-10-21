<script setup lang="ts">
import BaseLayout from '@/layouts/BaseLayout.vue';

import FranchiseSection from '@/components/section/FranchiseSection.vue';
import HeroSection from '@/components/section/HeroSection.vue';
import QualityFoodSection from '@/components/section/QualityFoodSection.vue';
import SupportSection from '@/components/section/SupportSection.vue';
import WelcomeSection from '@/components/section/WelcomeSection.vue';
import WhereFindUsSection from '@/components/section/WhereFindUsSection.vue';



</script>

<template>
    <BaseLayout>
        <HeroSection />

        <WelcomeSection />

        <QualityFoodSection />

        <FranchiseSection />

        <SupportSection />

        <WhereFindUsSection />
    </BaseLayout>
</template>
