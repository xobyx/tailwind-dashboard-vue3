<template>
<span @click="updateTheme">
  <component :is="theme?SunIcon:MoonIcon" class="top-navigation-icon" size="24"/>

    </span>
</template>
<script setup>
//import {MoonIcon,SunIcon} from '@heroicons/vue/24/solid'
import {inject} from "vue"
import {MoonIcon, SunIcon} from '@zhuowenli/vue-feather-icons'

const { theme, updateTheme } = inject('theme')
// eslint-disable-next-line no-unused-vars
</script>