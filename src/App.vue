<template>
  <div class="flex">
    <SideBar/>
    <Channelbar/>
    <ContentContainer/>
  </div>
</template>

<script>
import ChannelBar from "@/components/ChannelBar";
import SideBar from "@/components/SideBar";
import ContentContainer from "@/components/ContentContainer";
export default {
  mounted() {
  },
  name: 'App',
  components: {
    Channelbar: ChannelBar,SideBar,ContentContainer
}
}
</script>

