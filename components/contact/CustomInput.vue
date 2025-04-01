<template>
  <div class="relative w-full">
    <!-- Label -->
    <label
      :for="placeholder"
      class="text-xs text-gray-600 absolute -top-2 left-3"
    >
      {{ placeholder }}
    </label>

    <!-- Input Field -->
    <input
      v-if="type == 'text'"
      :id="placeholder"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      type="text"
      class="w-full px-3 pt-1 pb-2 rounded-t-sm hover:bg-black hover:opacity-10 border-b border-primary-blue text-primary-blue hover:text-white hover:font-semibold focus:outline-none focus:border-black"
    />
    <textarea
      v-if="type == 'textarea'"
      :id="placeholder"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      type="text"
      class="w-full h-24 px-3 pt-1 pb-2 rounded-t-sm hover:bg-black hover:opacity-10 border-b border-primary-blue text-primary-blue hover:text-white hover:font-semibold focus:outline-none focus:border-black"
    >
    </textarea>
  </div>
</template>

<script setup>
defineProps(["modelValue", "placeholder", "type"]);
defineEmits(["update:modelValue"]);
</script>
