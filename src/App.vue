<script >
  import HelloWorld from './components/HelloWorld.vue'
import NotifTab from './components/notif-tab.vue'
import image1 from './assets/assets/images/avatar-mark-webber.webp'
import image2 from './assets/assets/images/avatar-angela-gray.webp'
import image3 from './assets/assets/images/avatar-jacob-thompson.webp'
import AddedText from './components/AddedText.vue'


export default{
components:{
  HelloWorld,
  NotifTab,
  AddedText
},
data() {
    return {
      image1,
      image2,
      image3
    };
  },
}

</script>

<template>
  <div class="card-container" >
<NotifTab postee="Mark Webber" action="reacted to your recent post" event="My first Tournament today!" :src='image1' timeSent="1m ago" />
<NotifTab postee="Angela Gray" action="followed you" :src="image2" timeSent='5m ago' />
<NotifTab postee="Jacob Thompson" action="has joined your group" event="Chess Club" :src="image3" timeSent='1 day ago' />
<NotifTab postee="Jacob Thompson" action="has joined your group" event="Chess Club" :src="image3" timeSent='1 day ago' v-bind:myComponent="AddedText" />

  </div>
</template>

<style scoped>
.card-container {
display: flex;
  gap: 1em;
  flex-direction: column;
width: 60%;
margin: auto;
padding: 1em 1.5em;
background: white;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
