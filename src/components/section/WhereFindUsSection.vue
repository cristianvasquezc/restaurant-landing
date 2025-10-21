<script setup lang="ts">
import Section from '@/components/ui/Section.vue';
import Subtitle from '@/components/ui/Subtitle.vue';


</script>

<template>
    <Section>
        <n-grid x-gap="300" y-gap="40" cols="1 s:2" responsive="screen" class="text-white">
            <n-gi class="space-y-5">
                <Subtitle align="left">
                    Our Restaurants.
                    <br />
                    Where to Find Us?
                </Subtitle>
                <p class="text-lg">
                    Want to have a superb meal in an exceptional setting with family, friends or work colleagues, here
                    are the addresses of our restaurants.
                </p>
                <n-button round color="white" text-color="black">
                    Find The Nearest Cheffest
                </n-button>
            </n-gi>
            <n-gi>
                <div class="rounded-xl overflow-hidden aspect-square">
                    <iframe
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2229.603372596633!2d175.2726316383421!3d-37.7868681851146!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6d6d18a7bba18423%3A0xf00ef62249d27e0!2sSeddon%20Park!5e0!3m2!1ses-419!2spe!4v1761082303758!5m2!1ses-419!2spe"
                        width="100%" height="100%" style="border:0;"
                        referrerpolicy="no-referrer-when-downgrade"></iframe>
                </div>
            </n-gi>
        </n-grid>
    </Section>
</template>