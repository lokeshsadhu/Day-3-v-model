<script setup>
import { computed } from 'vue'

const props = defineProps({
  placeholder: String,
  name :{
    type:String,
    default:"No Name"
  }
})

const emit = defineEmits(['update:name'])
const proxyValue = defineModel()
</script>

<template>
  <input
    type="text"
    v-model="proxyValue"
    :placeholder="placeholder"
  />
</template>