<template lang="">
   <!-- <div>
      {{firstName}} {{lastName}}{{objectData}}
   </div> -->
   <h1>This is the componet</h1>
   <slot></slot>
</template>
<script>
export default {
   // props:["firstName","lastName","objectData"]

   // alt
   props:{
      firstName: String,
      lastName:String ,
      objectData:Object
   }
}
</script>
<style lang="">
   
</style>