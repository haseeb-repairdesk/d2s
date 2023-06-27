<template>
  <div class="dd-flex dd-items-center dd-justify-center">
    <dd-group-button
    :buttons="buttons"
    :showIcon="showIcon"
  />
  </div>
</template>

<script setup>
import DdGroupButton from "../groupButton/index.vue";

const props = defineProps({
    buttons: {
        type: Array,
        required: true
    }
})
</script>

<style>

</style>