<template>
  <div>
    <Navbar />
    <div class="container mx-auto mt-24 px-10">
      <EventDashboard />
    </div>
  </div>
</template>

<script setup lang="ts">
import EventDashboard from '@/features/events/dashboard/event-dashboard.vue';
import Navbar from '@/app/layouts/nav/navbar.vue';
</script>
