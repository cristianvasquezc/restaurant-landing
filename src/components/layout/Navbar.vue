<script setup lang="ts">
import logo from '@/assets/Logo.svg'
import { SearchRound, ShoppingCartRound } from '@vicons/material'
import { Icon } from '@vicons/utils'
import { onBeforeUnmount, onMounted, ref } from 'vue'
import { useRoute, useRouter } from 'vue-router'

const router = useRouter()
const route = useRoute()

const navLinks = [
    { label: 'Welcome', to: 'welcome', type: 'id' },
    { label: 'Our Menu', to: 'menu', type: 'id' },
    { label: 'Franchise', to: 'franchise', type: 'id' },
    { label: 'Contact', to: '/contact', type: 'route' }
]

const activeSection = ref<string>('welcome')

const handleNavClick = async (link: { to: string; type: string }) => {
    if (link.type === 'route') {
        router.push(link.to)
    } else if (link.type === 'id') {
        if (route.path !== '/') {
            await router.push('/')
            setTimeout(() => {
                document.getElementById(link.to)?.scrollIntoView({ behavior: 'smooth' })
            }, 300)
        } else {
            document.getElementById(link.to)?.scrollIntoView({ behavior: 'smooth' })
        }
    }
}

onMounted(() => {
    const observer = new IntersectionObserver(
        (entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    activeSection.value = entry.target.id
                }
            })
        },
        {
            rootMargin: '-50% 0px -50% 0px',
            threshold: 0
        }
    )

    navLinks.forEach((link) => {
        if (link.type === 'id') {
            const el = document.getElementById(link.to)
            if (el) observer.observe(el)
        }
    })

    onBeforeUnmount(() => observer.disconnect())
})
</script>

<template>
    <nav class="w-full bg-black text-white flex justify-center py-2 px-5 sticky top-0 z-50">
        <n-flex class="w-full max-w-6xl" justify="space-between" align="center">
            <n-flex>
                <button v-for="link in navLinks" :key="link.to" @click="handleNavClick(link)" class="transition-colors"
                    :class="[
                        link.type === 'id' && activeSection === link.to
                            ? 'text-white font-semibold'
                            : 'text-gray-300 hover:text-white'
                    ]">
                    {{ link.label }}
                </button>
            </n-flex>

            <div class="w-14">
                <img :src="logo" alt="Restaurant logo" />
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