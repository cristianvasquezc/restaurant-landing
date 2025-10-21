<script setup lang="ts">
import Section from '@/components/ui/Section.vue';
import Subtitle from '@/components/ui/Subtitle.vue';


</script>

<template>
    <Section class="pb-10">
        <Subtitle class="mb-10">
            We believe in making quality food
        </Subtitle>
        <n-grid x-gap="12" y-gap="20" cols="1 s:4" responsive="screen" class="text-white">
            <n-gi>
                <n-flex vertical align="center" justify="center">
                    <h2 class="font-bold text-5xl">
                        2M+
                    </h2>
                    <p class="text-base">
                        Happy Customers
                    </p>
                </n-flex>
            </n-gi>
            <n-gi>
                <n-flex vertical align="center" justify="center">
                    <h2 class="font-bold text-5xl">
                        98%
                    </h2>
                    <p class="text-base">
                        Customer Satisfaction
                    </p>
                </n-flex>
            </n-gi>
            <n-gi>
                <n-flex vertical align="center" justify="center">
                    <h2 class="font-bold text-5xl">
                        20+
                    </h2>
                    <p class="text-base">
                        Our Branches
                    </p>
                </n-flex>
            </n-gi>
            <n-gi>
                <n-flex vertical align="center" justify="center">
                    <h2 class="font-bold text-5xl">
                        100+
                    </h2>
                    <p class="text-base">
                        Total Employees
                    </p>
                </n-flex>
            </n-gi>
        </n-grid>
    </Section>
</template>