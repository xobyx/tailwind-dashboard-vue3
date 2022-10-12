<template>
  <div class='post'>
    <div class='avatar-wrapper'>
      <img :src="randomAvatar()" alt='' class='avatar' />
    </div>

    <div class='post-content'>
      <p class='post-owner'>
        {{name}}
        <small class='timestamp'>{{timestamp}}</small>
      </p>
      <p class='post-text'>{{text}}</p>
    </div>
  </div>

</template>
<script setup>


function randomAvatar(){
      return "https://avatars.dicebear.com/api/open-peeps/"+ Math.round(Math.random() * 100) +".svg";
    }


// eslint-disable-next-line no-undef
  defineProps({
    name:String,
    timestamp:String,
    text:String,
  })

</script>