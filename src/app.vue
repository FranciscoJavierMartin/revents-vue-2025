<template>
  <div>
    <Navbar @open="isFormOpen = !isFormOpen" />
    <div class="container mx-auto mt-24 px-10">
      <EventDashboard :isFormOpen @close="isFormOpen = false" />
    </div>
  </div>
</template>

<script setup lang="ts">
import EventDashboard from '@/features/events/dashboard/event-dashboard.vue';
import Navbar from '@/app/layouts/nav/navbar.vue';
import { ref } from 'vue';

const isFormOpen = ref<boolean>(false);
</script>
