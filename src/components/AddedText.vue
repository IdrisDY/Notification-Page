<template>
   <p>   Hello, thanks for setting up the Chess Club. I've been a member for a few weeks now and 
  I'm already having lots of fun and improving my game.
</p>
</template>

<script setup>

</script>

<style scoped>
p{
  font-size: 1rem;
  border: 1px solid hsl(219, 14%, 70%);
  width: 88%;
  margin-left: auto;
  padding: 1em;
  border-radius: .3em;
  color: hsl(219, 21%, 35%);
}
p:hover{
  background-color: hsl(205, 33%, 90%);
  cursor: pointer;
}
@media(max-width:550px){
  p{
    width: 80%;
  }
}
  @media(max-width:480px){
  p{
    width: 77%;
  }

}
@media(max-width:400px){
  p{
    width: 70%;
  }

}


</style>