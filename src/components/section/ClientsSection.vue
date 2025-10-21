<script setup lang="ts">
import ClientCard from '@/components/common/ClientCard.vue'
import Section from '@/components/ui/Section.vue'
import Subtitle from '@/components/ui/Subtitle.vue'

interface Client {
    name: string
    role: string
    avatar: string
    rating: number
    comment: string
}

const clients: Client[] = [
    {
        name: 'Michal Gun',
        role: 'Head of Sales at Tesla',
        avatar: 'https://randomuser.me/api/portraits/men/4.jpg',
        rating: 5,
        comment: "There are many variatioof passages of Lorem Ipsum ava but the majority If you are going to use a passage of Lorem Ipsum, you need tasure there isn't anything embarrassinhidden in believable."
    },
    {
        name: 'Aleena White',
        role: 'Accountant of Ozone ',
        avatar: 'https://randomuser.me/api/portraits/women/26.jpg',
        rating: 5,
        comment: "There are many variatioof passages of Lorem Ipsum ava but the majority If you are going to use a passage of Lorem Ipsum, you need tasure there isn't anything embarrassinhidden in believable."
    },
    {
        name: 'Cries Lee',
        role: 'CEO Of Montee',
        avatar: 'https://randomuser.me/api/portraits/women/90.jpg',
        rating: 5,
        comment: "There are many variatioof passages of Lorem Ipsum ava but the majority If you are going to use a passage of Lorem Ipsum, you need tasure there isn't anything embarrassinhidden in believable."
    },
    {
        name: 'Emily Carter',
        role: 'UX Designer at Adobe',
        avatar: 'https://randomuser.me/api/portraits/women/11.jpg',
        rating: 3,
        comment: "There are many variatioof passages of Lorem Ipsum ava but the majority If you are going to use a passage of Lorem Ipsum, you need tasure there isn't anything embarrassinhidden in believable."
    },
    {
        name: 'Daniel Kim',
        role: 'Software Engineer at Amazon',
        avatar: 'https://randomuser.me/api/portraits/men/51.jpg',
        rating: 4,
        comment: "There are many variatioof passages of Lorem Ipsum ava but the majority If you are going to use a passage of Lorem Ipsum, you need tasure there isn't anything embarrassinhidden in believable."
    },
    {
        name: 'Olivia Brown',
        role: 'Creative Director at Spotify',
        avatar: 'https://randomuser.me/api/portraits/women/79.jpg',
        rating: 5,
        comment: "There are many variatioof passages of Lorem Ipsum ava but the majority If you are going to use a passage of Lorem Ipsum, you need tasure there isn't anything embarrassinhidden in believable."
    },
]
</script>

<template>
    <Section>
        <Subtitle class="mb-10">
            What Our Clients Are Saying
        </Subtitle>

        <n-grid x-gap="20" y-gap="20" cols="1 s:3" responsive="screen" class="text-white">
            <n-gi v-for="client in clients" :key="client.name">
                <ClientCard :data="client" />
            </n-gi>
        </n-grid>
    </Section>
</template>
