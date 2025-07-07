<template>
  <div class="flex w-full flex-row gap-6">
    <div class="flex w-3/5 flex-col gap-4">
      <EventCard v-for="event of events" :key="event.id" :event />
    </div>
    <div class="w-2/5">
      <EventForm v-if="isFormOpen" @cancel="$emit('close')" />
    </div>
  </div>
</template>

<script setup lang="ts">
import EventCard from '@/features/events/dashboard/event-card.vue';
import EventForm from '@/features/events/form/event-form.vue';
import { events } from '@/lib/data/sample-data';

defineProps<{ isFormOpen: boolean }>();
defineEmits<{ close: void }>();
</script>
