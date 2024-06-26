<template lang="">
  <div>
    <h1>Count -><span>{{counter}}</span></h1>
    <button @click="(increment)">Increment</button>
    <!-- alt -->
    <!-- <button @click="this.counter++">Increment</button> -->
    <button @click="(decrement)">dencrement</button>
    <!-- attatch js value to an attribute tag -->
    <img v-bind:src="imgUrl">
   <!-- class styling binding -->
 <h4 :class="{hello:check}">conditional rendering</h4>
    <!-- conditional rendering -->
    <h1 v-show="check">This contains the v-show</h1>
    <button @click="changeState()">change state</button>
  <h1 v-if="check">The value is true</h1>
  
  <h1 v-else>The value is false</h1>
  
    <ul>
      <!-- looping through an array using dot notation -->
<!-- <li v-for="Object in Objects" :key="Object">{{Object.message}}</li> -->
<!-- alt, destructuring -->
<li v-for="({message},index) in Objects" :key="index">{{message}}</li>
    </ul>
    <!-- one way data binding -->
    <h3 >{{oneWayText}}</h3>
     <!-- two way data binding -->
    <h3 >{{twoWayText}}</h3>
      <input type="text" v-model="twoWayText">
    
  </div>
 <!-- <info-comp first-name="hehe" last-name="hehehehehehe"/>
 <info-comp first-name="hehe1"/>
 <info-comp :object-data="singleObject"/> -->
 <info-comp>
  Hehe I am using slots
 </info-comp>
  <slot-comp>
    <template #slotTitle>
      CARD Slot
    </template>
    <template #default>
      <img :src="imgUrl">
    </template>
  </slot-comp>
</template>
<script>
import SlotComp from '../components/SlotComp.vue';
import InfoComp from '../components/InfoComp.vue';


export default {
  data(){
    return{
      counter:0,
      imgUrl:"https://media.istockphoto.com/id/1470664921/photo/artificial-intelligence-processor-unit-powerful-quantum-ai-component-on-pcb-motherboard-with.jpg?s=612x612&w=0&k=20&c=8_6kBchV4R-I9cuyEQ78rIKWqHfk3e-zgnmVUrD8DkY=",
      check:true,
      sports:["soccer","netball","cricket"],
      Objects:[
        {message:'Hello There 1',id:1},
        {message:'Hello There 2',id:2},
        {message:'Hello There 3',id:3}
      ],
      singleObject:{
        name:"olwethu",
        surname:"Malumla",
      },
      oneWayText:"hehe",
      twoWayText:"hehe2.0"

    }
  },
  components:{
    InfoComp,
    SlotComp

  },
  methods:{
    increment(){
      this.counter+=5
    },
  decrement(){
      this.counter--
    },
  changeState(){
    this.check =!this.check
  }

  }
}
</script>
<style scoped>
h1{
  color:rgb(3, 177, 12)
}
.hello{
  color:rgb(16, 119, 175)
}
img{
  width:15rem
}
</style>
