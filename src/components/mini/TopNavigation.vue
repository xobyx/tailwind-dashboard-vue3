<template>
  <div class='top-navigation'>
    <HashIcon size="20" class="title-hashtag"></HashIcon>
    <h5 class='title-text'>{{ title }}</h5>
    <ThemeIcon/>

    <SearchItem/>

    <BellIcon size="24" class='top-navigation-icon' />
    <UserXIcon size="24" class='top-navigation-icon' />
  </div>

</template>

<script setup>
//import {ref} from "vue"
import SearchItem from "@/components/mini/SearchItem.vue";
import ThemeIcon from "@/components/mini/ThemeIcon.vue";
//import {UserCircleIcon,BellIcon,HashtagIcon} from "@vue-hero-icons/solid"
//import {} from '@heroicons/vue/solid/HashtagIcon'
//import {UserCircleIcon,BellIcon} from '@heroicons/vue/24/solid'
import {HashIcon,BellIcon,UserXIcon} from '@zhuowenli/vue-feather-icons'
// eslint-disable-next-line no-undef
defineProps(['title'])
//const title=ref("tailwind-css");

</script>

