<script setup lang="ts">
import FoodCard from '@/components/common/FoodCard.vue';
import Section from '@/components/ui/Section.vue';
import Subtitle from '@/components/ui/Subtitle.vue';
import { ref } from 'vue';

const foods = [
    {
        name: 'Naan Burger',
        description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
        image: new URL('@/assets/images/menu/naan-burger.webp', import.meta.url).href,
        price: 1.85
    },
    {
        name: 'Butter Chicken Taco',
        description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
        image: new URL('@/assets/images/menu/butter-chicken-taco.webp', import.meta.url).href,
        price: 1.15
    },
    {
        name: 'Chicken Burger',
        description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
        image: new URL('@/assets/images/menu/chicken-burger.webp', import.meta.url).href,
        price: 2
    },
    {
        name: 'Cheese Chicken Naan',
        description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
        image: new URL('@/assets/images/menu/cheese-chicken-naan.webp', import.meta.url).href,
        price: 2.5
    },
    {
        name: '3 Layer Burger',
        description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
        image: new URL('@/assets/images/menu/three-layer-burger.webp', import.meta.url).href,
        price: 4.99
    },
    {
        name: 'Sandwich',
        description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
        image: new URL('@/assets/images/menu/sandwich.webp', import.meta.url).href,
        price: 2.8
    }
]

const categories = ['All', 'Bread', 'Chiffon & Rolls', 'Donut', 'Pastry & Danish', 'Cakes', 'Cookies']

const activeCategory = ref('All')

const setActiveCategory = (category: string) => {
    activeCategory.value = category
}

</script>

<template>
    <Section id="menu" class="pb-10">
        <Subtitle class="mb-10">
            Our Best & Delicious Menu
        </Subtitle>

        <n-flex align="center" justify="space-between" class="mb-10">
            <button v-for="category in categories" :key="category"
                class="rounded-lg text-white px-3.5 transition-colors" :class="{
                    'border-b-2 border-white': activeCategory === category
                }" @click="setActiveCategory(category)">
                {{ category }}
            </button>
        </n-flex>

        <n-grid x-gap="20" y-gap="20" cols="1 s:3" responsive="screen" class="text-white">
            <n-gi v-for="(food, index) in foods" :key="index">
                <FoodCard :item="food" />
            </n-gi>
        </n-grid>

        <div class="mt-5 text-center">
            <n-button round color="white" text-color="black">
                See All
            </n-button>
        </div>
    </Section>
</template>
