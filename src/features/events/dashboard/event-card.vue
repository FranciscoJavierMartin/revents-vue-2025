<template>
  <div class="card card-border bg-base-100 w-full">
    <div class="card-body">
      <div class="flex items-center gap-3">
        <figure class="card-figure w-14 rounded-lg">
          <img
            src="https://img.daisyui.com/images/profile/demo/batperson@192.webp"
          />
        </figure>
        <div>
          <h2 class="card-title">Event Title</h2>
          <p class="text-neutral text-sm">Hosted by Bob</p>
        </div>
      </div>
      <div class="bg-base-200 border-neutral/20 -mx-6 my-3 border-y px-4 py-2">
        <EventAttendees />
      </div>
      <p>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Consectetur
        culpa accusantium ab dolores, aliquam nobis dolorem in placeat cumque!
        Error dolorum pariatur illo itaque, tempore quam similique esse porro
        atque?
      </p>
      <div class="card-actions flex">
        <div class="flex flex-1">Description</div>
        <button class="btn btn-primary"></button>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import EventAttendees from '@/features/events/dashboard/event-attendees.vue';
</script>
