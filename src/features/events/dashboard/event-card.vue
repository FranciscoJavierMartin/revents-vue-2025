<template>
  <div class="card card-border bg-base-100 w-full">
    <div class="card-body">
      <div class="flex items-center gap-3">
        <figure class="card-figure w-14 rounded-lg">
          <img :src="host?.photoURL || '/user.png'" />
        </figure>
        <div>
          <h2 class="card-title">{{ event.title }}</h2>
          <p class="text-neutral text-sm">Hosted by {{ host?.displayName }}</p>
        </div>
      </div>
      <div class="bg-base-200 border-neutral/20 -mx-6 my-3 border-y px-4 py-2">
        <EventAttendees :attendees="event.attendees" />
      </div>
      <div class="card-actions flex">
        <div class="flex flex-1">{{ event.description }}</div>
        <button class="btn btn-primary">View</button>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import EventAttendees from '@/features/events/dashboard/event-attendees.vue';
import type { AppEvent, Attendee } from '@/lib/types';
import { computed } from 'vue';

const props = defineProps<{ event: AppEvent }>();
const host = computed<Attendee | undefined>(() =>
  props.event.attendees.find((attendee) => attendee.isHost),
);
</script>
