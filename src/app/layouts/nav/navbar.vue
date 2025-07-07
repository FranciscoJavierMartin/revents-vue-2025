<template>
  <header
    class="from-primary fixed top-0 z-50 w-full bg-gradient-to-r to-black p-3"
  >
    <div
      class="mx-auto flex cursor-pointer items-center gap-6 px-10 align-middle"
    >
      <a
        href="#"
        class="flex max-h-16 items-center gap-3 border-r-2 border-r-white pr-6 text-white"
      >
        <h3 class="text-2xl font-semibold text-white uppercase">Re-vents</h3></a
      >
      <nav class="my-2 flex gap-3 text-lg text-white uppercase">
        <a>Events</a>
        <a @click="$emit('open')">Create</a>
      </nav>
      <div class="ml-auto flex gap-3 align-middle">
        <button class="btn">Login</button>
        <button class="btn">Register</button>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
defineEmits<{ open: void }>();
</script>
