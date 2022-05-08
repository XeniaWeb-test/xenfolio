<script setup>
import BaseLayout from '@/Layouts/Base';
import { Head } from '@inertiajs/inertia-vue3';

</script>

<template>
    <Head title="About"/>

    <BaseLayout>
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                My contacts
            </h2>
        </template>
        <div class="bg-red-100 p-20">
            <h1 class="text-red-700 text-lg font-semibold m-20">Contacts</h1>
        </div>
    </BaseLayout>
</template>

<style scoped>

</style>
