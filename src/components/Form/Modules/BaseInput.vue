<template>
  <div class="flex flex-col">
    <label
      v-if="label"
      class="text-sm font-medium text-[white]"
    >
      {{ label }}
    </label>
    <input
      :type="type"
      :placeholder="placeholder"
      :value="value"
      @input="handleInput"
      class="border border-gray-300 rounded-md px-3 py-2 mt-2 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-blue-500"
    />
  </div>
</template>

<script>
export default {
  name: "BaseInput",
  props: {
    value: {
      type: [String, Number],
      default: ""
    },
    label: {
      type: String,
      default: ""
    },
    placeholder: {
      type: String,
      default: ""
    },
    type: {
      type: String,
      default: "text"
    }
  },
  methods: {
    handleInput(event) {
      const val = event.target.value;
      console.log("input  with value:", val);
      this.$emit("input", val);
    }
  }
};
</script>
