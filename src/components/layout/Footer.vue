<script setup lang="ts">
import PaymentLogo from '@/components/icons/PaymentLogo.vue';
import { Discord, Facebook, Linkedin, Twitter } from '@vicons/fa';

</script>

<template>
    <footer class="bg-secondary text-white flex justify-center py-20 px-5">
        <div class="w-full max-w-6xl space-y-10">
            <n-grid x-gap="12" y-gap="20" cols="1 s:4" responsive="screen">
                <n-gi>
                    <h3 class="text-lg font-semibold mb-3">
                        Our Products
                    </h3>
                    <ul>
                        <li>
                            Our Menu
                        </li>
                        <li>
                            Our burgers
                        </li>
                        <li>
                            Our times sides
                        </li>
                        <li>
                            Our sandwiches
                        </li>
                    </ul>
                </n-gi>
                <n-gi>
                    <h3 class="text-lg font-semibold mb-3">
                        legal information
                    </h3>
                    <ul>
                        <li>
                            Legal Notice
                        </li>
                    </ul>
                </n-gi>
                <n-gi>
                    <h3 class="text-lg font-semibold mb-3">
                        Contact us
                    </h3>
                    <ul>
                        <li>
                            Contacts
                        </li>
                        <li>
                            Our addresses
                        </li>
                        <li>
                            Become a Times Square franchisee
                        </li>
                    </ul>
                </n-gi>
                <n-gi>
                    <h3 class="text-lg font-semibold mb-3">
                        We accept
                    </h3>
                    <n-flex size="large">
                        <PaymentLogo name="mastercard" />
                        <PaymentLogo name="visa" />
                        <PaymentLogo name="american-express" />
                    </n-flex>
                </n-gi>
            </n-grid>

            <div
                class="w-full flex flex-col sm:flex-row items-center justify-between gap-5 border-t border-tertiary pt-3">
                <n-flex>
                    <n-icon class="text-lg">
                        <Facebook />
                    </n-icon>
                    <n-icon class="text-lg">
                        <Twitter />
                    </n-icon>
                    <n-icon class="text-lg">
                        <Discord />
                    </n-icon>
                    <n-icon class="text-lg">
                        <Linkedin />
                    </n-icon>
                </n-flex>
                <p>© {{ new Date().getFullYear() }} Nayef All rights reserved.</p>
            </div>
        </div>
    </footer>
</template>