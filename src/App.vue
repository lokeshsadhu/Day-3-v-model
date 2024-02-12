<script setup>
import { ref } from 'vue'
import InputText from './components/InputText.vue'
import InputCheckbox from './components/InputCheckbox.vue'
import InputRadio from "@/components/InputRadio.vue"

const name = ref('Lokesh')
const newsletter = ref(false)
const radioletter = ref("male")
</script>

<template>
  <div>
    <h1>V-Model</h1>
    <form>
      <div>
        <InputText placeholder="Name" v-model="name" text="name"/>
        <div class="heading">Name: {{ name }}</div>
      </div>
      <hr/>
      <div>
        <div class="box">
         <h2>Click the Checkbox : </h2>
         <InputCheckbox v-model="newsletter" class="check"/>
        </div>
        <h2 class="heading">Checkbox clicked : {{ newsletter }}</h2>
      </div>
      <hr/>
      <div>
        <div class="box">
         <h2>Select One : </h2>
         <InputRadio v-model="radioletter" class="check"/>
        </div>
        <h2 class="heading">Selected Option : {{ radioletter }}</h2>
      </div>
      
    </form>
  </div>
</template>


<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.heading{
  font-size: 20px;
}
input {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  font-size: 16px;
  outline: none;
}
.box{
  display: flex;
  padding-bottom: 40px;
  flex-direction: row;
}
.check{
  margin-top: 10px;
  margin-left: 20px;
}
input:hover,
input:focus {
  border-color: #007bff;
  box-shadow: 0 0 5px rgba(0, 123, 255, 0.5);
}

</style>