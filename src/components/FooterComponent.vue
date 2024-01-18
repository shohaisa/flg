<script setup>
import { onMounted, ref } from 'vue'
const message = ref('')
onMounted(() => {
  fetch('https://www.boredapi.com/api/activity').then((response) => {
    return response.json()
  }).then((data) => {
    console.log(data)
    message.value = data.activity
  }).catch((err) => {
    console.log(err)
  })
})
</script>

<template>
<div>
  {{ message }}
</div>
</template>

<style scoped>

</style>
