<script >
import HelloWorld from "./components/HelloWorld.vue";
import NotifTab from "./components/notif-tab.vue";
import image1 from "./assets/assets/images/avatar-mark-webber.webp";
import image2 from "./assets/assets/images/avatar-angela-gray.webp";
import image3 from "./assets/assets/images/avatar-jacob-thompson.webp";
import image4 from "./assets/assets/images/avatar-rizky-hasanuddin.webp";
import image5 from "./assets/assets/images/avatar-kimberly-smith.webp";
import image6 from "./assets/assets/images/avatar-nathan-peterson.webp";
import image7 from "./assets/assets/images/avatar-anna-kim.webp";
import AddedText from "./components/AddedText.vue";
import headerVue from "./components/header.vue";
import chessImg from './assets/assets/images/image-chess.webp'
export default {
  components: {
    HelloWorld,
    NotifTab,
    AddedText,
    headerVue
  },
  data() {
    const marked = false
    const notifs = 3
    return {
      image1,
      image2,
      image3,
      image4,
      image5,
      image6,
      image7,
      AddedText,
      marked,
      notifs,
      chessImg
    };
  },
  methods:{
    markRead(){
      setTimeout(() => {
        this.notifs = 0;
    this.marked = true
      }, 200);
    }
  }
};
</script>

<template>
  <div class="card-container">
    <header-vue :count= 'notifs' @markRead = 'markRead' />
    <NotifTab
      postee="Mark Webber"
      action="reacted to your recent post"
      :read="marked"
      event="My first Tournament today!"
      :src="image1"
      timeSent="1m ago"
    />
    <NotifTab
      postee="Angela Gray"
      action="followed you"
      :src="image2"
      :read="marked"
      timeSent="5m ago"
    />
    <NotifTab
      postee="Jacob Thompson"
      action="has joined your group"
      event="Chess Club"
      :read="marked"
      :src="image3"
      timeSent="1 day ago"
    />
    <NotifTab
      postee="Risky Hasanuddin"
      action="has joined your group"
      event="Chess Club"
      :read="true"
      :src="image4"
      timeSent="5 days ago"
      :some-prop="AddedText"
    />
    <NotifTab
      postee="Kimberly Smith"
      action="commented on your picture"
      :read="true"
      :src="image5"
      timeSent="1 week ago"
      :img="chessImg"
    />
    <NotifTab
      postee="Nathan Peterson"
      action="reacted to your recent post"
      event="5 end-game strategies to increase your win rate."
      :read="true"
      :src="image6"
      timeSent="2 weeks ago"
    />
    <NotifTab
      postee="Anna Kim"
      action="left the group"
      event="Chess Club."
      :read="true"
      :src="image7"
      timeSent="2 weeks ago"
    />

  </div>
</template>

<style scoped>
.card-container {
  display: flex;
  gap: 1em;
  flex-direction: column;
  width: 60%;
  margin: auto;
  padding: 2em 1.5em;
  background: white;
}
@media(max-width:768px) {
.card-container{
  width: 90%;
  padding: 1em;
}
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
