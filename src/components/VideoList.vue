<template>
  <ul class="list-group col-lg-4">
    <VideoListItem
      v-for="video in videos"
      :key="video.etag"
      :video="video"
      @videoSelect="onVideoSelect"
    ></VideoListItem>
  </ul>
</template>
<script>
import VideoListItem from './VideoListItem';
export default {
  name: 'Videolist',
  components: {
    VideoListItem,
  },
  props: ['videos'],
  methods:{
    onVideoSelect(video){
      this.$emit('videoSelect',video)
    }
  }
};
</script>

<style></style>
