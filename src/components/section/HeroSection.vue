<template>
    <section class="relative text-white h-screen">
        <img src="@/assets/images/background.webp" alt="Background"
            class="absolute inset-0 w-full h-full object-cover object-center" />

        <div class="absolute inset-0 bg-black/20"></div>

        <div class="relative z-10 flex items-center justify-center h-full px-5">
            <div class="w-full max-w-6xl mx-auto">
                <div class="max-w-lg space-y-5">
                    <h1 class="text-3xl md:text-5xl leading-tight font-black">
                        Welcome!
                        <br />
                        We Made Delicious Food for You
                    </h1>
                    <p class="text-lg">
                        Lorem Ipsum is simply dummy text of the printing and typesetting industry.
                    </p>
                    <n-button round color="white" text-color="black">
                        Order Online
                    </n-button>
                </div>
            </div>
        </div>
    </section>
</template>
