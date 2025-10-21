<script setup lang="ts">
import Section from '@/components/ui/Section.vue';
import Subtitle from '@/components/ui/Subtitle.vue';


</script>

<template>
    <Section class="bg-white">
        <Subtitle class="text-black">
            For more Support
        </Subtitle>

        <n-flex align="center" justify="center">
            <n-input round placeholder="Enter Email" class="border"
                style="--n-text-color: black; --n-placeholder-color: black; max-width: 300px;" />
            <n-button round color="black" text-color="white">
                Subscribe
            </n-button>
        </n-flex>
    </Section>
</template>