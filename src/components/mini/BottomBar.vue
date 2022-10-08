<template>
  <div class='bottom-bar'>
    <PlusIcon
        size='22'
        class='text-green-500 dark:shadow-lg mx-2 dark:text-primary'
    />

    <input type='text' placeholder='Enter message...' class='bottom-bar-input'/>
  </div>
</template>
<script>
//import {PlusIcon} from '@heroicons/vue/solid'
import {PlusIcon} from '@zhuowenli/vue-feather-icons'
export default {
  name: 'BottomBar',
  components:{PlusIcon}
}
</script>