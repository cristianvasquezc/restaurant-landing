<script setup lang="ts">
import Section from '@/components/ui/Section.vue';
import Subtitle from '@/components/ui/Subtitle.vue';


</script>

<template>
    <Section id="franchise" class="pb-10">
        <div class="flex flex-col items-center">
            <Subtitle class="max-w-2xl mx-auto">
                Start The Adventure Today And Become a Franchisee
            </Subtitle>
            <p class="text-lg text-center text-white mb-10 ">
                Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the
                industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and
                scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap
                into
                electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the
                release of
                Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like
                Aldus PageMaker including versions of Lorem Ipsum.
            </p>
            <n-button round color="white" text-color="black">
                Become a Franchisee
            </n-button>
        </div>
    </Section>
</template>