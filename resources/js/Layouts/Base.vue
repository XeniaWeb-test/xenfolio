<script setup>
import { ref } from 'vue';
import AppLogoXeniaWeb from '@/Components/AppLogoXeniaWeb.vue';
import BreezeNavLink from '@/Components/NavLink.vue';
import {Link} from '@inertiajs/inertia-vue3';
</script>

<template>
    <div class="min-h-screen bg-gray-100  dark:bg-gray-900">
        <!-- Primary Navigation Menu -->
        <nav class="bg-purple-200 relative flex justify-between py-4 px-[5%] border-b border-purple-700">
            <!-- Logo -->
            <div class="shrink-0 flex items-center">
                <Link href="/">
                    <AppLogoXeniaWeb class="block w-auto h-12 fill-current"/>
                </Link>
            </div>
            <!-- Navigation Links -->
            <div class="hidden space-x-8 sm:-my-px sm:ml-10 sm:flex">
                <BreezeNavLink :href="route('web-works.index')" :active="route().current('web-works/index')">
                    My Works
                </BreezeNavLink>
                <BreezeNavLink :href="route('page.about')" :active="route().current('page.about')">
                    About me
                </BreezeNavLink>
                <BreezeNavLink :href="route('page.contacts')" :active="route().current('page.contacts')">
                    Contacts
                </BreezeNavLink>
            </div>
        </nav>
        <!-- Page Heading -->
        <header class="bg-white shadow" v-if="$slots.header">
            <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
                <slot name="header" />
            </div>
        </header>

        <main>
            <slot/>
        </main>

        <footer class="">
            <div class="bg-purple-500 py-4 px-[5%]">
                <p class="py-10 text-white font-semibold border-4 border-gray-100 ">This is Footer</p>
            </div>
        </footer>
    </div>
</template>
