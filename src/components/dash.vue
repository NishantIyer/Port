<template>
  <div class="full-screen-image"></div>
</template>

<script>
export default {
  name: 'FullScreenImage',
};
</script>

<style>
.full-screen-image {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('https://pbs.twimg.com/media/DVHhlY9XcAEIntE?format=jpg&name=4096x4096');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
