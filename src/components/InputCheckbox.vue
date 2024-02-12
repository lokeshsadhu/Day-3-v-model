<script setup>

const props = defineProps({
  newsletter: Boolean
})

const emit = defineEmits(['update:newsletter'])
const newValue=defineModel()
</script>

<template>
  <input
    type="checkbox"
    v-model="newValue"
    class="box"
  />
</template>

<style>
.box{
    height: 20px;
    widows: 20px;
    padding-top: 5px;
}
</style>