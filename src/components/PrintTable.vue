<template>
  <div>
    <div v-for="(list, index) in fullInfo" :key="index">
      <div v-if="list.indexOf(search) != -1">
        <input v-model="fullInfoCopy[index]">
        <ButtonThisSettings @click.native="changeInfo" text="Редактировать"/>
        <ButtonThisSettings @click.native="deleteInfo(index)" text="Удалить"/>
      </div>
    </div>
  </div>

</template>

<script>
import ButtonThisSettings from "@/components/ButtonThisSettings";
export default {
  components: {ButtonThisSettings},
  props: {
    fullInfo: {
      type: Array
    },
    search: {
      type: String,
      required: false,
      default: ""
    }
  },
  data(){
    return{
      fullInfoCopy: this.fullInfo,
      displayChange: false,

    }
  },
  methods: {
    changeInfo(){
      this.$emit('new-info', this.fullInfoCopy);
    },
    deleteInfo(index){

      alert(this.fullInfoCopy);
      alert(index);

      alert(this.fullInfoCopy);

      this.$emit('new-info', this.fullInfoCopy);
    },

  }
}
</script>

<style scoped>

</style>


