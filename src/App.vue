<template>
  <div class="flex">
    <SideBar />
    <ChannelBar />
    <ContentContainer />
  </div>
</template>

<script setup>
import { provide, ref, watchEffect } from 'vue'

import ChannelBar from "@/components/ChannelBar";
import SideBar from "@/components/SideBar";
import ContentContainer from "@/components/ContentContainer";
const theme = ref(JSON.parse(localStorage.getItem('dark-theme'))|| 0)
function updateTheme() {
  theme.value = !theme.value;
}
watchEffect(() => {
  try {
    const className = 'dark';
    const bodyClass = window.document.body.classList;

    theme.value ? bodyClass.add(className) : bodyClass.remove(className);
    localStorage.setItem('dark-theme', JSON.stringify(theme.value));
  } catch (error) {
    console.log(error);
  }
})

provide('theme', {
  theme,
  updateTheme
});

const channelp = ref('');
function updatechannel(r)
{
  channelp.value = r;
}

provide('channelp', {
  channelp,
  updatechannel
});

</script>

