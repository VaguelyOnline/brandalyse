<script setup>
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
import { Link } from '@inertiajs/vue3';

const bgClass = Math.random() > 0.5 ? 'guest-bg': 'bg-gradient-to-r from-indigo-500 from-10% via-sky-500 via-30% to-emerald-500 to-90%';

</script>

<style scoped>
    .guest-bg {
        background-image: url(https://images.unsplash.com/photo-1721959525992-d9da99585c89?q=80&w=1500&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D);
        background-size: cover;
    }
</style>

<template>
    <div
    :class="bgClass"
        class="flex min-h-screen flex-col items-center  pt-6 sm:justify-center sm:pt-0 dark:bg-gray-900"
    >
        <div>
            <Link href="/">
                <!-- <ApplicationLogo class="h-20 w-20 fill-current text-gray-500" /> -->
                <h1 class="font-extrabold text-xl mb-5 text-gray-100">
                    BRANDALYSE
                </h1>
            </Link>
        </div>

        <div
            class="mt-6 w-full overflow-hidden glass bg-white opacity-90 px-6 py-4 shadow-md sm:max-w-md sm:rounded-lg dark:bg-gray-800"
        >
            <slot />
        </div>
    </div>
</template>
