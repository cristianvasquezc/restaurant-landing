<script setup lang="ts">
import { QuoteLeft } from '@vicons/fa'
import { StarRound, } from '@vicons/material'

interface Data {
    name: string
    role: string
    avatar: string
    rating: number
    comment: string
}

const props = defineProps<{
    data: Data
}>()
</script>

<template>
    <div class="bg-secondary p-5 rounded-lg">
        <n-flex align="center">
            <n-avatar round :size="55" :src="props.data.avatar" />
            <n-flex vertical size="small">
                <h3 class="text-lg font-semibold leading-none">
                    {{ props.data.name }}
                </h3>
                <p class="leading-none">
                    {{ props.data.role }}
                </p>
                <div class="flex">
                    <n-icon v-for="i in 5" :key="i" class="transition-colors duration-200"
                        :class="i <= props.data.rating ? 'text-orange-400' : 'text-gray-400 opacity-50'">
                        <StarRound />
                    </n-icon>
                </div>
            </n-flex>
        </n-flex>

        <div class="flex my-1.5">
            <n-icon>
                <QuoteLeft />
            </n-icon>
            <div class="w-full my-1 border-b border-tertiary" />
        </div>

        <p>
            {{ props.data.comment }}
        </p>
    </div>
</template>
