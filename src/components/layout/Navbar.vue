<script setup lang="ts">
import logo from '@/assets/Logo.svg'
import { MenuRound, SearchRound, ShoppingCartRound } from '@vicons/material'
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
const menuOpen = ref(false)
const scrolled = ref(false)

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

    const onScroll = () => {
        scrolled.value = window.scrollY > 50
    }

    window.addEventListener('scroll', onScroll)

    onBeforeUnmount(() => observer.disconnect())
})
</script>

<template>
    <nav :class="[
        'w-full fixed top-0 left-0 right-0 z-50 transition-colors duration-300',
        scrolled || menuOpen ? 'bg-black' : 'bg-transparent md:bg-black'
    ]" class="text-white py-2 px-5">
        <div class="flex justify-between items-center max-w-6xl mx-auto py-2 px-5">
            <button class="md:hidden" @click="menuOpen = !menuOpen">
                <Icon size="24">
                    <MenuRound />
                </Icon>
            </button>

            <div class="hidden md:flex space-x-6">
                <button v-for="link in navLinks" :key="link.to" @click="handleNavClick(link)" class="transition-colors"
                    :class="[
                        link.type === 'id' && activeSection === link.to
                            ? 'text-white font-semibold'
                            : 'text-gray-300 hover:text-white'
                    ]">
                    {{ link.label }}
                </button>
            </div>

            <div class="w-14">
                <img :src="logo" alt="Restaurant logo" />
            </div>

            <n-flex align="center" size="large">
                <RouterLink to="/cart" v-slot="{ isActive }">
                    <n-badge :value="2">
                        <Icon :class="isActive ? 'text-white' : 'text-white'" size="24">
                            <ShoppingCartRound />
                        </Icon>
                    </n-badge>
                </RouterLink>

                <button class="hidden md:block">
                    <Icon size="24">
                        <SearchRound />
                    </Icon>
                </button>

                <RouterLink to="" class="bg-white text-black px-5 rounded-full py-1.5 hidden md:block">
                    Become a Member
                </RouterLink>
            </n-flex>
        </div>

        <div v-if="menuOpen" class="md:hidden">
            <div class="flex flex-col space-y-2 px-5 pb-4">
                <button v-for="link in navLinks" :key="link.to" @click="handleNavClick(link)"
                    class="text-gray-300 hover:text-white text-left"
                    :class="link.type === 'id' && activeSection === link.to ? 'text-white font-semibold' : ''">
                    {{ link.label }}
                </button>
            </div>
        </div>
    </nav>
</template>