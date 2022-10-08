<template>
  <div class="fixed top-0 left-0 h-screen w-16 flex flex-col
                  bg-white dark:bg-gray-900 shadow-lg">


    <SideBarIcon icon="MusicIcon" size="28" text="tooltip 💡" />
    <hr class="sidebar-hr" />
    <SideBarIcon icon="BarChartIcon" size="32" text="tooltip 💡" />
    <SideBarIcon icon="HashIcon" size="20" text="tooltip 💡" />
    <SideBarIcon icon="CloudLightningIcon" size="20" text="tooltip 💡" />
    <hr class="sidebar-hr" />
    <SideBarIcon icon="PlusIcon" size="22" text="tooltip 💡" />
  </div>

</template>
<script>

import SideBarIcon from "./mini/SideBarIcon";
export default {
  name: 'SideBar',
  components: {SideBarIcon}
}
</script>