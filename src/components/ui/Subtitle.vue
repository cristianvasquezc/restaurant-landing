<script setup lang="ts">
import { twMerge } from 'tailwind-merge';
import { computed } from 'vue';

const props = defineProps<{
    align?: 'left' | 'center' | 'right'
    class?: string
}>()

const subtitleClass = computed(() =>
    twMerge(
        'font-bold text-2xl md:text-4xl text-white mb-5',
        props.align ? `text-${props.align}` : 'text-center',
        props.class
    )
)
</script>

<template>
    <h2 :class="subtitleClass">
        <slot />
    </h2>
</template>
