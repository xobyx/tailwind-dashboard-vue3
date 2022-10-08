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

<script>
import SearchItem from "@/components/mini/SearchItem";
import ThemeIcon from "@/components/mini/ThemeIcon";
//import {UserCircleIcon,BellIcon,HashtagIcon} from "@vue-hero-icons/solid"
//import {} from '@heroicons/vue/solid/HashtagIcon'
//import {UserCircleIcon,BellIcon} from '@heroicons/vue/24/solid'
import {HashIcon,BellIcon,UserXIcon} from '@zhuowenli/vue-feather-icons'
export default {
  name: "TopNavigation",
  components: {ThemeIcon, SearchItem,UserXIcon,BellIcon,HashIcon},
  data(){
    return {
      title:"tailwind - css"
    }
  }
}
</script>

