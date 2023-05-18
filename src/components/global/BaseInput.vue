<template>
  <div class="input-wrapper">
    <label v-if="label" class=""
      >{{ label }}<span v-if="isRequired">*</span></label
    >
    <input
      id="inputField"
      :class="{ 'pr-34 input-width-with-icon': showIcon }"
      v-bind="$attrs"
      :value="value"
      @input="updateInputValue"
      :required="isRequired"
    />

    <!-- icon slot only accept image for now -->
    <div
      :class="
        showIcon
          ? label.length
            ? 'inputIcon'
            : 'inputIcon-without-label'
          : 'inputIcon'
      "
      v-if="showIcon"
    >
      <slot name="icon" class="icon"></slot>
    </div>
  </div>
</template>

<script>
export default {
  inheritAttrs: false,
  props: {
    label: {
      type: String,
      default: "",
    },
    value: [String, Number],

    // show icon is required if passing icon slot to add icon in input field
    showIcon: {
      type: Boolean,
      default: false,
    },
    isRequired: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    updateInputValue(event) {
      this.$emit("input", event.target.value);
    },
  },
};
</script>

<style scoped>
.input-wrapper {
  position: relative;
}
label {
  font-size: 14px;
  font-weight: 500;
  color: var(--gray-color);
  display: block;
  margin-bottom: 0.3rem;
}

input {
  width: calc(100% - 20px);
  height: 35px;
  border-radius: calc(var(--border-radius) / 3);
  border: 1px solid var(--light-gray-color);
  padding: 0 10px;
}

.input-width-with-icon {
  width: calc(100% - 45px);
}
.pr-34 {
  padding-right: 34px;
}

input:focus,
input:active {
  outline: none;
}

.inputIcon {
  position: absolute;
  top: 22px;
  right: 0;
}

.inputIcon-without-label {
  position: absolute;
  top: 0;
  right: 0;
}
.inputIcon .icon,
.inputIcon-without-label img,
.inputIcon img {
  height: 20px;
  width: 20px;
  margin: 7px;
}
</style>
