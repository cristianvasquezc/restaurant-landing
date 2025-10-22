<script setup lang="ts">
import { ShoppingCartOutlined } from '@vicons/material'

interface FoodItem {
    name: string
    description: string
    image: string
    price: number
}

const props = defineProps<{
    item: FoodItem
}>()
</script>

<template>
    <div class="bg-secondary p-5 rounded-lg">
        <div class="aspect-[4/3] flex items-center justify-center mb-3">
            <img :src="props.item.image" :alt="props.item.name" class="w-2xs h-full object-cover" />
        </div>
        <h3 class="text-xl font-bold mb-2">
            {{ props.item.name }}
        </h3>

        <p class="mb-5 text-base">
            {{ props.item.description }}
        </p>

        <n-flex align="center" justify="space-between">
            <h3 class="text-xl font-bold text-white">
                ${{ props.item.price.toFixed(2) }}
            </h3>
            <n-button circle text-color="white">
                <n-icon>
                    <ShoppingCartOutlined />
                </n-icon>
            </n-button>
        </n-flex>
    </div>
</template>
