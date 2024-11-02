<template>

  <label class="checkbox-wrapper">
    <input type="checkbox" v-model="isChecked" @change="handleChange" />
    <span class="custom-checkbox"></span>
  </label>

</template>

<script>
export default {
  data() {
    return {
      isChecked: false, 
    };
  },
  methods: {
    handleChange() {
      console.log("Checkbox is checked:", this.isChecked);
    },
  },
};
</script>

<style scoped>

input[type="checkbox"] {
  display: none;
}

.custom-checkbox {
  width: 23px;
  height: 23px;
  border: 1px solid #000;
  display: inline-block;
  position: relative;
  cursor: pointer;
  padding: 5px;
}


.custom-checkbox::after {
  content: "";
  position: absolute;
  left: 7px;
  top: 2px;
  width: 6px;
  height: 12px;
  border-right: 1px solid #000;
  border-bottom: 1px solid #000;
  transform: rotate(45deg);
  opacity: 0;
  transition: opacity 0.2s;
}

input[type="checkbox"]:checked + .custom-checkbox::after {
  opacity: 1;
}
</style>