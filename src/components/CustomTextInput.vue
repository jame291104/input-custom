<template>
  <label :for="inputName">
    <input
      :name="inputName"
      type="text"
      :placeholder="placeholder"
      :value="inputValue"
      v-on:input="handleInput"
    />
  </label>
</template>

<script>
export default {
  name: "CustomTextInput",
  props: {
    inputName: String,
    inputValue: String,
    placeholder: String
  },
  methods: {
    handleInput(event) {
      
      this.$emit("input", event.target.value);
    },
  },
};
</script>