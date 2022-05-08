<script setup>
import {ref} from 'vue';
import AppLogoXeniaWeb from '@/Components/AppLogoXeniaWeb.vue';
import BreezeNavLink from '@/Components/NavLink.vue';
import SocialLink from '@/Components/SocialLink.vue';
import {Link} from '@inertiajs/inertia-vue3';
</script>

<template>
    <div class="min-h-screen bg-gray-100  dark:bg-gray-900">
        <!-- Primary Navigation Menu -->
        <nav class="bg-purple-200 relative flex justify-between py-4 px-[5%] border-b border-purple-700">
            <!-- Logo -->
            <div class="group shrink-0 flex items-center">
                <Link href="/">
                    <AppLogoXeniaWeb color-web="blue-950" class="block w-auto h-12 group-hover:fill-blue-950/60"/>
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
            <div class="max-w-7xl mx-auto py-6 px-[5%] ">
                <slot name="header"/>
            </div>
        </header>

        <main>
            <slot/>
        </main>

        <footer class="">
            <div class="relative flex justify-between py-4 px-[5%] border-b">
                <div class="flex">
                    <ul class="flex mr-auto pt-1 pr-4 justify-start items-center align-middle flex-wrap sm:flex-nowrap">
                        <SocialLink href="https://www.linkedin.com/in/xeniaweb" title="Xenia on Linkedin">
                            <svg width="15.74" height="15.05" viewBox="0 0 15.74 15.05">
                                <path class="fill-blue-950  group-hover:fill-blue-950/50"
                                      d="M15.87,15.52V9.7c0-3.12-1.66-4.57-3.88-4.57A3.36,3.36,0,0,0,8.94,6.81V5.37H5.57c0,1,0,10.15,0,10.15H8.94V9.85A2.29,2.29,0,0,1,9.06,9,1.82,1.82,0,0,1,10.79,7.8c1.22,0,1.71.93,1.71,2.29v5.44ZM2,4A1.76,1.76,0,1,0,2,.47,1.76,1.76,0,1,0,2,4ZM3.7,15.52V5.37H.33V15.52Z"
                                      transform="translate(-0.13 -0.47)"/>
                            </svg>
                        </SocialLink>
                        <SocialLink href="https://www.youtube.com/channel/UCKSXl_LlBNShvPMrxCDIcYw"
                                    title="Xenia on Youtube">
                            <svg x="0px" y="0px" width="19.979px fill-blue-500" height="14.015px"
                                 viewBox="0 0 19.979 14.015">
                                <path class="fill-blue-950  group-hover:fill-blue-950/50"
                                      d="M17.145,0H2.835C1.275,0,0,1.275,0,2.835v8.345c0,1.56,1.275,2.835,2.835,2.835h14.31c1.56,0,2.835-1.275,2.835-2.835V2.835 C19.979,1.275,18.704,0,17.145,0z M7.036,10.392V3.623l6.769,3.384L7.036,10.392z"/>
                            </svg>
                        </SocialLink>
                    </ul>
                </div>
                <div class="group block cursor-pointer sm:flex justify-center items-center py-3 align-middle">
                    <small class="block py-2 mr-3 group-hover:text-blue-950/50">developed by </small>
                    <a class="cursor-pointer z-50" href="https://xeniaweb.ch/" target="_blank" title="Xenia WEB">
                        <span class="sr-only">Oksana Burki</span>
                        <Link href="/">
                            <AppLogoXeniaWeb color-web="blue-950" class="w-auto h-10 group-hover:fill-blue-950/50"/>
                        </Link>
                    </a>
                </div>
            </div>
        </footer>
    </div>
</template>

<style scoped>


</style>
