<script setup>
import Hero from '@/components/Hero.vue'
import HomeCards from '@/components/HomeCards.vue'
import JobListings from '@/components/JobListings.vue'
</script>

<template>
    <!-- <Hero title="" subtitle=""/> -->
    <Hero/>
    <HomeCards/>
    <JobListings :limit="5 " :show-button="true"/>
</template>