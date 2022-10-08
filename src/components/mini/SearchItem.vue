<template>
  <div class='search'>
    <input class='search-input' type='text' placeholder='Search...'/>
    <SearchIcon size='18' class='text-secondary my-auto'/>
  </div>
</template>
<script>
//import { SearchIcon} from '@heroicons/vue/solid'
import {SearchIcon} from '@zhuowenli/vue-feather-icons'
export default {
  components:{SearchIcon},
  name: 'SearchItem'
}
</script>
