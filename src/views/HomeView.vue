<script setup lang="ts">
import BaseLayout from '@/layouts/BaseLayout.vue';

import ClientsSection from '@/components/section/ClientsSection.vue';
import FranchiseSection from '@/components/section/FranchiseSection.vue';
import HeroSection from '@/components/section/HeroSection.vue';
import MenuSection from '@/components/section/MenuSection.vue';
import QualityFoodSection from '@/components/section/QualityFoodSection.vue';
import SupportSection from '@/components/section/SupportSection.vue';
import WelcomeSection from '@/components/section/WelcomeSection.vue';
import WhereFindUsSection from '@/components/section/WhereFindUsSection.vue';


</script>

<template>
    <BaseLayout>
        <HeroSection />

        <WelcomeSection />

        <MenuSection />

        <QualityFoodSection />

        <FranchiseSection />

        <ClientsSection />

        <SupportSection />

        <WhereFindUsSection />
    </BaseLayout>
</template>
