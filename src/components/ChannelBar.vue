<!--suppress JSUnusedGlobalSymbols -->
<template>
  <div class='channel-bar shadow-lg'>
    <div class='channel-block'>
      <h5 class='channel-block-text'>Channels</h5>
    </div>
    <div class='channel-container'>
      <DropDown header='Topics' :selections="topics" />
      <DropDown header='Questions' :selections="questions" />
      <DropDown header='Random' :selections="random" />
    </div>
  </div>
</template>
<script setup>
/* eslint-disable */

import DropDown from "@/components/mini/DropDown";
const topics = ['tailwind-css', 'vue.js'];
const questions = ['jit-compilation', 'purge-files', 'dark-mode'];
const random = ['variants', 'plugins'];


</script>