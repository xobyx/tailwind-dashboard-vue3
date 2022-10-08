<template>
<span @click="darkTheme=!darkTheme">
  <component :is="darkTheme?'SunIcon':'MoonIcon'" class="top-navigation-icon" size="24"/>

    </span>
</template>
<script>
//import {MoonIcon,SunIcon} from '@heroicons/vue/24/solid'
import {MoonIcon,SunIcon} from '@zhuowenli/vue-feather-icons'
export default {
  components:{SunIcon,MoonIcon},
  name: 'ThemeIcon',
  data(){
    return {
      darkTheme: ()=>{const item=window.localStorage.getItem('dark-theme');
        return item ? JSON.parse(item) : true;},
    }
  },
  computed:{
    /*
    mode(){
      try {
        const item = window.localStorage.getItem('dark-theme');
        return item ? JSON.parse(item) : true;
      } catch (error) {
        console.log(error);
        return false;
      }

    }
      */
  },
  methods:
      {

      },
  watch:{
    // eslint-disable-next-line no-unused-vars
    darkTheme(newValue,oldValue)
    {
      try {
        const className = 'dark';
        const bodyClass = window.document.body.classList;

        newValue ? bodyClass.add(className) : bodyClass.remove(className);
        window.localStorage.setItem('dark-theme', JSON.stringify(newValue));
      } catch (error) {
        console.log(error);
      }

    }
  },
  mounted() {
    try {
      const className = 'dark';
      const bodyClass = window.document.body.classList;

      this.darkTheme ? bodyClass.add(className) : bodyClass.remove(className);
      window.localStorage.setItem('dark-theme', JSON.stringify(this.darkTheme));
    } catch (error) {
      console.log(error);
    }
  }
}
</script>