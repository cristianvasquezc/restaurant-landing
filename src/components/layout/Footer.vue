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
                    <n-ul align-text>
                        <n-li>
                            Our Menu
                        </n-li>
                        <n-li>
                            Our burgers
                        </n-li>
                        <n-li>
                            Our fries
                        </n-li>
                        <n-li>
                            Our sandwiches
                        </n-li>
                    </n-ul>
                </n-gi>
                <n-gi>
                    <h3 class="text-lg font-semibold mb-3">
                        legal information
                    </h3>
                    <n-ul align-text>
                        <n-li>
                            Legal Notice
                        </n-li>
                    </n-ul>
                </n-gi>
                <n-gi>
                    <h3 class="text-lg font-semibold mb-3">
                        Contact us
                    </h3>
                    <n-ul align-text>
                        <n-li>
                            Contacts
                        </n-li>
                        <n-li>
                            Our addresses
                        </n-li>
                        <n-li>
                            Become a Times Square franchisee
                        </n-li>
                    </n-ul>
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