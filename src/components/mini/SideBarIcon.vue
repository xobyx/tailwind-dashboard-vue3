<template>
  <div class="sidebar-icon group">
    <div class="sidebar-tab-cont">
      <span
        class="sidebar-tab" :class="{'sidebar-tab-active':active}"></span>
    </div>
    <component :is="icon" :size="size" />
    <span class="sidebar-tooltip group-hover:scale-100">
      {{text}}
    </span>
  </div>
</template>
<script setup>




// eslint-disable-next-line no-undef
defineProps({
  icon: Object, size: String, text: String,active:Boolean
})

</script>