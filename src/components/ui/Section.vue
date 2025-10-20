<script setup lang="ts">
import { twMerge } from 'tailwind-merge';
import { computed } from 'vue';

const props = defineProps<{
    id?: string
    class?: string
}>()

const sectionClass = computed(() =>
    twMerge('bg-primary py-20 px-5', props.class)
)
</script>

<template>
    <section :id="props.id" :class="sectionClass">
        <div class="max-w-6xl mx-auto">
            <slot />
        </div>
    </section>
</template>
