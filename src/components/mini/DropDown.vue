<template>
  <div class='dropdown'>
    <div @click="expanded=!expanded" class='dropdown-header'>
    <component :is="expanded?'ChevronDownIcon':'ChevronRightIcon'" class="text-accent text-opacity-80 my-auto mr-1" />
    <h5
        :class="expanded ? 'dropdown-header-text-selected' : 'dropdown-header-text'"
    >
    {{header}}
    </h5>
    <PlusIcon size='12' class='text-accent text-opacity-80 my-auto ml-auto' />
  </div>

    <slot v-if="expanded&&selections">
    <div class='dropdown-selection' v-for="sel in selections" :key="sel">

        <HashIcon size='24' class='text-gray-400' />
        <h5 class='dropdown-selection-text'>{{sel}}</h5>
    </div>
    </slot>
  </div>
</template>

<script>
//import { PlusIcon,HashtagIcon,ChevronDownIcon,ChevronRightIcon} from '@heroicons/vue/solid'
import {PlusIcon,HashIcon,ChevronDownIcon,ChevronRightIcon} from '@zhuowenli/vue-feather-icons'
export default {
  name: "DropDown",
  components:{HashIcon,PlusIcon,ChevronDownIcon,ChevronRightIcon},
  data(){
    return {
      expanded: false
    }
  },
  props:{
    header:String,selections:Array
  }
}
</script>

<style scoped>

</style>