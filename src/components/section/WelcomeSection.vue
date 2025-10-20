<script setup lang="ts">
import Section from '@/components/ui/Section.vue';
import Subtitle from '@/components/ui/Subtitle.vue';
import { PlayArrowRound } from '@vicons/material';

import { ref } from 'vue';

const showModal = ref(false)

</script>

<template>
    <Section id="welcome">
        <Subtitle text="Why We Are the Best Food Makers" />
        <p class="text-lg text-center text-white mb-10 max-w-2xl mx-auto">
            Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem scrambled it to make a type
            specimen book.
        </p>
        <n-grid x-gap="80" y-gap="20" cols="1 s:2" responsive="screen" class="text-white">
            <n-gi>
                <p class="text-lg text-center md:text-start">
                    It is a long established fact that a reader will be distracted layout. The point of using Lorem
                    Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using English.
                    Many desktop publishing packages and web page editors now use Lorem Ipsum as their default model
                    text, and a search for 'lorem ipsum' will uncover many web sites still in their infancy. Various
                    versions have evolved over the years, sometimes by accident, sometimes on purpose It is a long
                    established fact that a reader will be distracted by the readable content of a page when looking at
                    its layout. The normal distribution of letters, as opposed to using 'Content Many desktop publishing
                    packages and web page editors search for 'lorem ipsum' will uncover many web sites still in humour
                    and the like. <span class="font-bold">Read More</span>
                </p>
            </n-gi>
            <n-gi>
                <div class="relative rounded-xl overflow-hidden">
                    <img src="@/assets/images/video-cover.webp" alt="Video Cover" class="w-full h-auto" />
                    <div
                        class="absolute inset-0 flex items-center justify-center bg-black/20 hover:bg-black/40 transition">
                        <button class="bg-white w-10 h-10 rounded-full flex items-center justify-center"
                            @click="showModal = true">
                            <n-icon class="text-4xl text-black">
                                <PlayArrowRound />
                            </n-icon>
                        </button>
                    </div>

                    <n-modal v-model:show="showModal" style="width: 800px" preset="card" :show-mask="false"
                        class="bg-red-500">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione, iste. Temporibus quae
                        inventore deleniti recusandae numquam neque eligendi culpa incidunt odio fuga eum molestias
                        corporis tenetur dicta explicabo, obcaecati excepturi!
                    </n-modal>
                </div>
            </n-gi>
        </n-grid>

    </Section>
</template>