<template>
  <div class="fixed top-0 left-0 h-screen w-16 flex flex-col
                  bg-white dark:bg-gray-900 shadow-lg">


    <SideBarIcon :icon="FolderIcon" size="28" text="tooltip 💡" :active="selected==0" @click="selected=0" />
    <hr class="sidebar-hr" />
    <SideBarIcon :icon="HashIcon" size="32" text="tooltip 💡" :active="selected==1" @click="selected=1"/>
    <SideBarIcon :icon="MusicIcon" size="20" text="tooltip 💡" :active="selected==2" @click="selected=2"/>
    <SideBarIcon :icon="CloudLightningIcon" size="20" text="tooltip 💡" :active="selected==3" @click="selected=3" />
    <hr class="sidebar-hr" />
    <SideBarIcon :icon="PlusIcon" size="22" text="tooltip 💡" :active="selected==4" @click="selected=4"/>
  </div>

</template>
<script setup>
import { ref } from 'vue';
import {PlusIcon,HashIcon,FolderIcon,CloudLightningIcon,MusicIcon} from '@zhuowenli/vue-feather-icons'
import SideBarIcon from "./mini/SideBarIcon";

var selected = ref(0);
</script>