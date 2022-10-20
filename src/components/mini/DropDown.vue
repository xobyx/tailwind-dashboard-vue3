<template>
  <div class='dropdown'>
    <div @click="expanded=!expanded" class='dropdown-header'>
    <component :is="expanded?ChevronDownIcon:ChevronRightIcon" class="text-accent text-opacity-80 my-auto mr-1" />
    <h5
        :class="expanded ? 'dropdown-header-text-selected' : 'dropdown-header-text'"
    >
    {{header}}
    </h5>
    <PlusIcon size='12' class='text-accent text-opacity-80 my-auto ml-auto' />
  </div>

    <template v-if="expanded&&selections">
    <div class='dropdown-selection' v-for="sel in selections" :key="sel" @click="$emit('dropdown_selection',sel)">

        <HashIcon size='24' class='text-gray-400' :class="{'text-green-400': i.split('>')[1]==sel}" />
        <h5 class='dropdown-selection-text'>{{sel}}</h5>
    </div>
    </template>
  </div>
</template>

<script setup>
//import { PlusIcon,HashtagIcon,ChevronDownIcon,ChevronRightIcon} from '@heroicons/vue/solid'
// eslint-disable-next-line no-unused-vars
import {PlusIcon,HashIcon,ChevronDownIcon,ChevronRightIcon} from '@zhuowenli/vue-feather-icons'


import { ref } from 'vue'
const expanded =ref(false);
// eslint-disable-next-line no-undef
defineProps({ header: String, selections: Array,i:String })
// eslint-disable-next-line no-undef
defineEmits(['dropdown_selection'])

</script>

<style scoped>

</style>