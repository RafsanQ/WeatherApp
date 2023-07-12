<template>
    <header class="sticky top-0 bg-weather-primary shadow-lg">
        <nav class="container flex flex-col sm:flex-row items-center gap-4 text-white py-6">
            <RouterLink :to="{name: 'home'}">
                <div class="flex items-center gap-3 flex-1">
                    <i class="fa-solid fa-sun text-2xl"></i>
                    <p class="text-2xl">The Local Weather</p>
                </div>
            </RouterLink>

            <div class="flex gap-3 flex-1 justify-end">
                <i class="fa-solid fa-circle-info hover:text-weather-secondary duration-150 cursor-pointer"></i>
                <i class="fa-solid fa-plus hover:text-weather-secondary duration-150 cursor-pointer"></i>
            </div>
            <BaseModal>
                <div class="text-black">
                    <h1 class="text-2xl mb-1">About:</h1>
                    <p class="mb-4">
                        The Local Weather page allows you to track the current and future weather of cities of your choosing.
                    </p>

                    <h2 class="text-xl">How it works:</h2>
                    <ol class="list-decimal list-inside mb-4">
                        <li>Search for your city by entering the name of your desired city into the search bar</li>

                        <li>Select a city from the results. This will take you to the current weather of that city.</li>

                        <li>Track the city by clicking on the '+' icon on the top right. This will save the city onto the homepage to view at a later time.</li>
                    </ol>

                    <h2 class="text-xl">Removing a city:</h2>
                    <p class="mv-4">
                        If you no longer wish to track a city, simply select it from the homepage and click on the delete option that will appear at the bottom of the page.
                    </p>
                </div>
            </BaseModal>
        </nav>
    </header>
</template>

<script setup>
    import { RouterLink } from 'vue-router';
    import BaseModal from './BaseModal.vue';
</script>
