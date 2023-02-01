<script setup>
import { ref } from 'vue'

defineProps({
  postee: String,
  action:String,
  event:String,
  src: String,
  timeSent:String,
  read:Boolean,
  someProp:Object,
})

const count = ref(0)



</script>

<template>
<div class="wrapper">
  <div class="card" :style="{ backgroundColor: read ? 'white' : 'hsl(211, 68%, 94%)' }">
   <div>
      <img :src="src" alt="profile-img" class="prof-pic" />
      </div>
   <div class='notif-info'>
      <div class="body">
         <div >
      <strong>{{postee}}</strong> <span class="action" >{{ action }}  </span> <span  :style="{color:event === 'Chess Club'?'hsl(219, 85%, 26%)':'hsl(219, 12%, 42%)', fontWeight:600 }" > {{event }}</span>
</div>
<p class="c-red" v-if="!read" > </p>
</div>
<span class="times" > {{timeSent }} </span>
</div>
</div>
<component :is="someProp"> </component>

  </div>

</template>

<style scoped>
.card{
   height: fit-content;
   border-radius: .5em;
   display: flex;
   padding: .8em .8em .3em .8em;
   gap: 1em;
}
.body{
   display: flex;
   align-items: center;
}
.c-red{
   min-width: 10px;
  min-height: 10px;
  border-radius: 50%;
  margin: 0 .5em;
  background-color: red;
text-align: center;
}
.prof-pic{
   height: 30px;
}
.notif-info{
   display: flex;
   flex-direction: column;
}
.times{
   color: hsl(219, 14%, 63%);
   font-size: .8rem;
}
.action{
   color: hsl(219, 21%, 35%);
   font-weight: 500;
}
</style>
