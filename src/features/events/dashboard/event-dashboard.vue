<template>
  <div class="flex w-full flex-row gap-6">
    <div class="flex w-3/5 flex-col gap-4">
      <EventCard v-for="i of 10" :key="i" />
    </div>
    <div class="w-2/5">
      <EventForm />
    </div>
  </div>
</template>

<script setup lang="ts">
import EventCard from '@/features/events/dashboard/event-card.vue';
import EventForm from '@/features/events/form/event-form.vue';
</script>
