<template>
  <div class="block relative">
  <div class="a group">
    <div class="sidebar-tab-continar">
      <span
        class="sidebar-tab" :class="{'sidebar-tab-active':active,'group-hover:h-8':!active}"></span>
    </div>
    <div class="sidebar-icon groub">
    <component :is="icon" :size="size" />
    <span class="sidebar-tooltip group-hover:scale-100">
      {{text}}
    </span>
  </div>
  </div>
</div>
</template>
<script setup>




// eslint-disable-next-line no-undef
defineProps({
  icon: Object, size: String, text: String,active:Boolean
})

</script>