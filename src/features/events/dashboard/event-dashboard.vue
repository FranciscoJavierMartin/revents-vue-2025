<template>
  <div class="flex w-full flex-row gap-6">
    <div class="flex w-3/5 flex-col gap-4">
      <EventCard v-for="event of appEvents" :key="event.id" :event />
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
import type { AppEvent } from '@/lib/types';
import { onBeforeUnmount, onMounted, ref } from 'vue';

const appEvents = ref<AppEvent[]>([]);

defineProps<{ isFormOpen: boolean }>();
defineEmits<{ close: void }>();

onMounted(() => {
  appEvents.value = events;
});

onBeforeUnmount(() => {
  appEvents.value = [];
});
</script>
