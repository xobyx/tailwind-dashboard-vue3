<template>
  <div class="sidebar-icon group">
    <component :is="icon" :size="size"/>
    <span class="sidebar-tooltip group-hover:scale-100">
      {{text}}
    </span>
  </div>
</template>
<script>
//import { PlusIcon,HashtagIcon,PhotographIcon,LightningBoltIcon} from '@heroicons/vue/solid'
import {PlusIcon,HashIcon,BarChartIcon,CloudLightningIcon,MusicIcon} from '@zhuowenli/vue-feather-icons'
export default {
  name: 'SideBarIcon',
  components:{PlusIcon,HashIcon,BarChartIcon,CloudLightningIcon,MusicIcon},
  props:{
    icon:String,size:String,text:String
  }
}
</script>