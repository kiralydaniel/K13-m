<template>    
    <nav class="bg-white border-gray-200 dark:bg-gray-900 fixed top-0 w-full z-50">
        <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
            <a href="/" class="flex items-center">
                <img src="/K13-MESTER_logo1.png" class="absolute left-25 top-0 w-28 md:z-30" alt="K13 MESTER Logo" />
            </a>
            <button id="navbar-toggle-button" data-collapse-toggle="navbar-default" type="button" class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="navbar-default" aria-expanded="false">
                <span class="sr-only">Open main menu</span>
                <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
                    <path  stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
                </svg>
            </button>
            <div class="hidden w-full md:block md:w-auto max-md:pt-5" id="navbar-default">
            <ul class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
                <li>
                <NuxtLink to="/" @click="closeMobileMenu" class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-sky-400 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Kezdőlap</NuxtLink>
                </li>
                <li>
                <NuxtLink to="kreak2" @click="closeMobileMenu" class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-sky-400 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Krea K2+</NuxtLink>
                </li>
                <li>
                <NuxtLink to="upgrade" @click="closeMobileMenu" class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-sky-400 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Korszerűsítés lépései</NuxtLink>
                </li>
                <li>
                <NuxtLink to="contact" @click="closeMobileMenu" class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-sky-400 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">Kapcsolat</NuxtLink>
                </li>
            </ul>
            </div>
        </div>
    </nav>
</template>


<script setup>
import { onMounted } from 'vue'
import { Collapse } from 'flowbite'

function closeMobileMenu() {
    const $targetEl = document.getElementById('navbar-default');
    const $triggerEl = document.getElementById('navbar-toggle-button');

    if ($targetEl) {
        const collapse = new Collapse($targetEl, $triggerEl, {
            toggleOnOpen: false,
            closeOnClick: true,
        });

        collapse.toggle();
    }
}

onMounted(() => {
    const $targetEl = document.getElementById('navbar-default');
    const $triggerEl = document.getElementById('navbar-toggle-button');

    if ($targetEl) {
        const collapse = new Collapse($targetEl, $triggerEl, {
            toggleOnOpen: false,
            closeOnClick: true,
        });
    }
})
</script>