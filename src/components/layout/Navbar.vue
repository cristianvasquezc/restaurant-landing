<script setup lang="ts">
import { SearchRound, ShoppingCartRound } from '@vicons/material';
import { Icon } from '@vicons/utils';
import { RouterLink } from 'vue-router';

import logo from '@/assets/Logo.svg';

interface NavLink {
    label: string
    to: string
}

const navLinks: NavLink[] = [
    { label: 'Welcome', to: '/' },
    { label: 'Our Menu', to: '/menu' },
    { label: 'Franchise', to: '/franchise' },
    { label: 'Contact', to: '/contact' }
]

</script>

<template>
    <nav class="w-full bg-black text-white flex justify-center py-2 px-5">
        <n-flex class="w-full max-w-6xl" justify="space-between" align="center">
            <n-flex>
                <RouterLink v-for="link in navLinks" :key="link.to" :to="link.to"
                    active-class="text-white font-semibold">
                    {{ link.label }}</RouterLink>
            </n-flex>

            <div class="w-14">
                <img :src="logo" alt=" Restaurant logo" />
            </div>

            <n-flex align="center">
                <RouterLink to="/cart" v-slot="{ isActive }">
                    <n-badge :value="2">
                        <Icon :class="isActive ? 'text-white' : 'text-white'" size="24">
                            <ShoppingCartRound />
                        </Icon>
                    </n-badge>
                </RouterLink>

                <n-button quaternary circle>
                    <n-icon class="text-2xl text-white">
                        <SearchRound />
                    </n-icon>
                </n-button>

                <n-button round color="white" text-color="black">
                    Become a Member
                </n-button>
            </n-flex>
        </n-flex>
    </nav>
</template>