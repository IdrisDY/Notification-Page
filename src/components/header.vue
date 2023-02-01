<template>
  <div class="head">
    <div class="notif">
      <h1>Notifications</h1>
      <span> {{ count }} </span>
    </div>
    <button @click="$emit('markRead')">Mark all as read</button>
  </div>
</template>

<script setup>
defineProps({
  count: Number,
});
</script>

<style scoped>
.head {
  display: flex;
  justify-content: space-between;
}
button {
  all: unset;
  cursor: pointer;
  font-size: 1rem;
}
button:hover {
  color: hsl(219, 85%, 26%);
}
h1 {
  font-size: 1.4rem;
  margin: 0;
}
.notif {
  display: flex;
  gap: 1em;
}
.notif span {
  background: hsl(219, 85%, 26%);
  color: white;
  font-size: 1rem;
  padding: 0 0.2em;
  border-radius: 0.5em;
  width: 18px;
  text-align: center;
  height: 100%;
}
@media (max-width: 768px) {
  h1 {
    font-size: 1rem;
  }
  .notif {
    gap: 0.5em;
  }
}
</style>