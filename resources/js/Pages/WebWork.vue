<script setup>
import BaseLayout from '@/Layouts/Base';
import { Head } from '@inertiajs/inertia-vue3';

</script>

<template>
    <Head title="WebWorks" />

    <BaseLayout>
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                What I Do
            </h2>
        </template>
        <div class="bg-blue-100 p-20">
            <h1 class="text-green-700 text-lg font-semibold m-20">My WebWork</h1>
        </div>
    </BaseLayout>
</template>

<style scoped>

</style>
