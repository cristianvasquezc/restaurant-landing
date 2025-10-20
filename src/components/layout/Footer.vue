<script setup lang="ts">
import PaymentLogo from '@/components/icons/PaymentLogo.vue';
import { Discord, Facebook, Linkedin, Twitter } from '@vicons/fa';

</script>

<template>
    <footer class="bg-secondary text-white flex justify-center py-10 px-2">
        <div class="w-full max-w-6xl space-y-10">
            <n-grid x-gap="12" cols="1 s:4" responsive="screen">
                <n-gi>
                    <n-h3>Our Products</n-h3>
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
                    <n-h3>legal information</n-h3>
                    <ul>
                        <li>
                            Legal Notice
                        </li>
                    </ul>
                </n-gi>
                <n-gi>
                    <n-h3>Contact us</n-h3>
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
                    <n-h3>We accept</n-h3>
                    <n-flex size="large">
                        <PaymentLogo name="mastercard" />
                        <PaymentLogo name="visa" />
                        <PaymentLogo name="american-express" />
                    </n-flex>
                </n-gi>
            </n-grid>

            <n-flex justify="space-between" align="center" class="border-t border-tertiary pt-3">
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
            </n-flex>
        </div>
    </footer>
</template>