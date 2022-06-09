<template>
  <div>
    <InputInfo v-model="text"></InputInfo>
    <ButtonThisSettings @click.native="clearInput" text="Click me"/>
  </div>
</template>

<script>
import ButtonThisSettings from "@/components/ButtonThisSettings";
import InputInfo from "@/components/InputInfo";
export default {
  components: {InputInfo, ButtonThisSettings},
  data(){
    return{
      text: "",
    }
  },
  methods: {
    clearInput(){
      this.$emit('new-info', this.text);
      this.text = '';
    }
  }


}
</script>

<style scoped>

</style>
