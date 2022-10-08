/* eslint-disable */
<template>
  <div class='content-container'>
    <TopNavigation/>
    <div class='content-list'>

      <PostItem name='Leon' timestamp='one week ago' text="Lorem ipsum dolor. " />

      <PostItem name='Jill' timestamp='5 days ago' text="Lorem." />
      <PostItem
          name='Ellie'
          timestamp='4 days ago'
          text="Lorem ipsum dolor sit amet consectetur adipisicing elit. "
      />
      <PostItem
          name='Chris'
          timestamp='4 days ago'
          text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem ipsum dolor sit
          amet consectetur adipisicing elit. Lorem ipsum dolor sit amet consectetur
          adipisicing elit. Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem
          ipsum dolor sit amet consectetur adipisicing elit.

          Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem
          ipsum dolor sit amet consectetur adipisicing elit."
      />
      <PostItem
          name='Claire'
          timestamp='2 days ago'
          text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem ipsum dolor sit
          amet consectetur adipisicing elit. Lorem ipsum dolor sit amet consectetur
          adipisicing elit. Lorem ipsum dolor sit amet consectetur adipisicing elit. "
      />
      <PostItem
          name='Albert'
          timestamp='22 hours ago'
          text="Lorem ipsum dolor sit amet consectetur adipisicing elit. ☺️ "
      />
      <PostItem
          name='Rebecca'
          timestamp='3 hours ago'
          text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem ipsum dolor sit
          amet consectetur adipisicing elit."
      />
      <PostItem
          name='H.U.N.K'
          timestamp='Just now'
          text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem ipsum dolor sit
          amet consectetur adipisicing elit. Lorem ipsum dolor sit amet consectetur
          adipisicing elit. Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem
          ipsum dolor sit amet consectetur adipisicing elit."
      />
    </div>
    <BottomBar/>

  </div>

</template>
<script>
import PostItem from "@/components/mini/PostItem";
import TopNavigation from "@/components/mini/TopNavigation";
import BottomBar from "@/components/mini/BottomBar";

export default {
  name: 'ContentContainer',
  components: {BottomBar, TopNavigation, PostItem}
}
</script>