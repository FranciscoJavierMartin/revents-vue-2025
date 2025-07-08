<template>
  <div class="card bg-base-100 flex w-full flex-col gap-3 p-4">
    <h3 class="text-primary text-center text-2xl font-semibold">
      Create new event
    </h3>
    <form @submit.prevent="onSubmit" class="flex w-full flex-col gap-3">
      <input
        name="title"
        type="text"
        placeholder="Event title"
        class="input input-lg w-full"
      />
      <input
        name="category"
        type="text"
        placeholder="Category"
        class="input input-lg w-full"
      />
      <textarea
        name="description"
        type="text"
        placeholder="Description"
        class="textarea textarea-lg w-full"
      />
      <input
        name="date"
        type="datetime-local"
        placeholder="Date"
        class="input input-lg w-full"
      />
      <input
        name="city"
        type="text"
        placeholder="City"
        class="input input-lg w-full"
      />
      <input
        name="venue"
        type="text"
        placeholder="Venue"
        class="input input-lg w-full"
      />
      <div class="flex w-full justify-end gap-3">
        <button class="btn btn-neutral">Cancel</button>
        <button class="btn btn-primary">Create</button>
      </div>
    </form>
  </div>
</template>

<script setup lang="ts">
defineEmits<{ close: void }>();

function onSubmit(e: Event): void {
  console.log('Form submittedmio', e);
}
</script>
