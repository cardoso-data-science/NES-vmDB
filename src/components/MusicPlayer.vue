<!-- MusicPlayer.vue -->
<template>
    <div>
      <audio :src="musicSource" controls></audio>
    </div>
  </template>
  
  <script>
  export default {
    name: 'MusicPlayer',
    props: {
      musicSource: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  /* Add styles specific to your music player */
  </style>
  