<script setup>
defineProps(['message'])
defineEmits(['messageEmitted'])
</script>

<template>
  <div class="border border-dashed rounded-lg p-4 mt-8 ml-8">
    <h6 class="font-semibold mb-4">Child Component</h6>
    <p class="text-sm text-gray-500 mb-4">{{ message }}</p>
    <button
      type="button"
      class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 focus:outline-none"
      @click="
        $emit(
          'messageEmitted',
          `I am a custom message generated on ${new Date().toLocaleString()}`
        )
      "
    >
      Generate Custom Message
    </button>
  </div>
</template>

<style scoped></style>
