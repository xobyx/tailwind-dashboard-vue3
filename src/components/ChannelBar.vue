<!--suppress JSUnusedGlobalSymbols -->
<template>
  <div class='channel-bar shadow-lg'>
    <div class='channel-block'>
      <h5 class='channel-block-text'>Channels</h5>
    </div>
    <div class='channel-container'>
      <DropDown header='Topics' :selections="topics" @dropdown_selection="sTopics" :i="channelp" />
      <DropDown header='Questions' :selections="questions" @dropdown_selection="sQuestions" :i="channelp" />
      <DropDown header='Random' :selections="random" @dropdown_selection="sRandom" :i="channelp"/>
    </div>
  </div>
</template>
<script setup>
import {inject} from 'vue'    
/* eslint-disable */

import DropDown from "@/components/mini/DropDown";
const topics = ['tailwind-css', 'vue.js'];
const questions = ['jit-compilation', 'purge-files', 'dark-mode'];
const random = ['variants', 'plugins'];
inject("theme");
const { channelp, updatechannel } = inject('channelp')

function sTopics(r)
{
  if(channelp!=0)
  updatechannel( 'Topics>' + r);
}
function sQuestions(r)
{
  updatechannel('Questions>' + r);
}
function sRandom(r)
{
  updatechannel('Random>' + r);
}
updatechannel('Topics>tailwind-css');
</script>