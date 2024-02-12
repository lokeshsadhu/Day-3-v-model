<template>
    <div class="box">
        <label>
            <input type="radio" name="gender" value="male" v-model="radioValue"> Male
        </label>
        <label>
            <input type="radio" name="gender" value="female" v-model="radioValue"> Female
        </label>
        <label>
            <input type="radio" name="gender" value="other" v-model="radioValue"> Other
        </label>
    </div>
</template>

<script setup>
import {ref} from "vue"

defineProps(["radioletter"])
const radioValue=defineModel()

</script>

<style>
.box{
    padding-top: 0px;
}
</style>