<script setup>
import { ref } from 'vue'

defineProps({
  postee: String,
  action:String,
  event:String,
  src: String,
  timeSent:String,
  myComponent:Object,
})

const count = ref(0)
</script>

<template>

  <div class="card">
   <div>
      <img :src="src" alt="profile-img" class="prof-pic" />
      </div>
   <div class='notif-info'>
      <div class="body">
         <div >
      <strong>{{postee}}</strong> <span class="action" >{{ action }}  </span> <span> {{event }}</span>
</div>
<p class="c-red"> </p>
</div>
<span class="times" > {{timeSent }} </span>
{{myComponent}}
</div>


  </div>

</template>

<style scoped>
.card{
   background:hsl(211, 68%, 94%);
   height: 10vh;
   border-radius: .5em;
   display: flex;
   align-items: center;
   padding: .3em .5em;
   gap: 1em;
}
.body{
   display: flex;
   align-items: center;
}
.c-red{
   width: 10px;
  height: 10px;
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
