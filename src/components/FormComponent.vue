<template>
  <input 
    id="firstName" 
    name="firstName"
    type="text"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    placeholder="firstName" >
</template>

<script>
export default {
  name: 'FormComponent',
  props: ['modelValue'],
}
</script>
