<template>
  <input v-model="text" @input="$emit('input', text);">
</template>

<script>
export default {
  data(){
    return{
      text: "",
    }
  }
}
</script>

<style scoped>

</style>
