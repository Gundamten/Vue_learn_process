<template>
  <div v-bind:id="dynamicID" v-bind:class="dynamicClass" v-bind:title="dynamicTitle">测试</div>
  <button :disabled="isButtonDisabled">Button</button>
  <div v-bind="objectOfAttrs">测试</div>
</template>
<script>
export default {
  data(){
    return{
      dynamicClass:"active",
      dynamicID:"appid",
      dynamicTitle:"hahaha",
      isButtonDisabled:false,
      objectOfAttrs:{
        dynamicClass:"active",
        dynamicID:"appid"
      }
    }
  }
}
</script>

