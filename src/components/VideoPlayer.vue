<!-- VideoPlayer.vue -->
<template>
  <div>
    <video :src="videoSource" controls></video>
  </div>
</template>

<script>
export default {
  name: 'VideoPlayer',
  props: {
    videoSource: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
/* Add styles specific to your video player */
</style>
