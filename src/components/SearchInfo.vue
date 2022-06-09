<template>
  <div>
    <input placeholder="Введите Поиск" v-model="textSearch" @input="searchInfoMethod">
  </div>
</template>

<script>
export default {
  components: {},
  data(){
    return{
      textSearch: "",
    }
  },
  methods: {
    searchInfoMethod(){
      this.$emit("add-search", this.textSearch)
    }
  }
}
</script>

<style scoped>

</style>
