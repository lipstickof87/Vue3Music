<template>
  <div class="container-mainLeft">
    <ul class="entry">
      
      <li @click="goFindMusic" class="entry-item">
        <a href="javascript:;">发现</a>
      </li>
      <li @click="goVideo" class="entry-item">
        <a href="javascript:;">视频</a>
      </li>
      <li @click="goPlayed" class="entry-item"><a href="javascript:;">播放</a></li>
      <!-- todo:后续加 -->
      <li  class="entry-item"><a href="javascript:;">喜欢</a></li>
      <li class="entry-item"><a href="javascript:;">收藏</a></li>
      <li class="entry-item"><a href="javascript:;">发现</a></li>
      <li  class="entry-item"><a href="javascript:;">歌单</a></li>
    </ul>
  </div>
</template>
<script setup lang="ts">
import { useRouter } from 'vue-router'

const router = useRouter()
const goFindMusic = () => {
  router.push('/ContainerMainFind')
}
const goVideo = () => {
  router.push('/ContainerMainVideo')
}
const goSongList = () => {
  router.push('/SongList')
}

const goPlayed = () => {
  router.push('/ContainerMainRecently')
}
</script>
<style lang="scss" scoped>
.container-mainLeft{
  opacity: 0.8;
}
.entry{
  overflow: hidden;
  
.entry-item{
  height: 14%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  a{
    color: rgb(221, 122, 180);
  }
}
}
</style>
