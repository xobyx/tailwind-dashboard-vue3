<template>
<span @click="darkTheme=!darkTheme">
  <component :is="darkTheme?SunIcon:MoonIcon" class="top-navigation-icon" size="24"/>

    </span>
</template>
<script setup>
//import {MoonIcon,SunIcon} from '@heroicons/vue/24/solid'
import {ref, onMounted, watch} from "vue"
import {MoonIcon, SunIcon} from '@zhuowenli/vue-feather-icons'
function mode () {
  const item = window.localStorage.getItem('dark-theme');

  return item ? JSON.parse(item) : true;
}
let darkTheme = ref(mode());
// eslint-disable-next-line no-unused-vars
watch(darkTheme, (newValue,__oldValue) => {
  try {
    const className = 'dark';
    const bodyClass = window.document.body.classList;

    newValue ? bodyClass.add(className) : bodyClass.remove(className);
    window.localStorage.setItem('dark-theme', JSON.stringify(newValue));
  } catch (error) {
    console.log(error);
  }
});

onMounted(() => {
  try {
    const className = 'dark';
    const bodyClass = window.document.body.classList;

    darkTheme.value ? bodyClass.add(className) : bodyClass.remove(className);
    window.localStorage.setItem('dark-theme', JSON.stringify(darkTheme.value));
  } catch (error) {
    console.log(error);
  }

});
</script>