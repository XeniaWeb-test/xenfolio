<script setup>
import {computed} from 'vue';

const props = defineProps(['href', 'title', 'social']);

</script>

<template>
    <li class="group hover:bg-blue-950/5 hover:border-blue-950/50 cursor-pointer border border-gray-400 rounded bg-transparent w-24 sm:w-11 h-24 sm:h-11 flex justify-center items-center my-3 mx-2">
        <a :href="href"
           target="_blank" title="{{ title }}">
            <span class="sr-only">{{ title }}</span>
            <slot/>
        </a>
    </li>
</template>
