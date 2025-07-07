<template>
  <div class="avatar-group -space-x-5">
    <div v-for="attendee of attendees" :key="attendee.id" class="avatar">
      <div class="w-12">
        <img :src="attendee.photoURL" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { Attendee } from '@/lib/types';

defineProps<{ attendees: Attendee[] }>();
</script>
