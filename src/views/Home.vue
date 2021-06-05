<template>
  <div class="home">
    <img
      class="bgbox"
      src="https://cdn.jsdelivr.net/gh/MobiusBeta/assets/images/BG_A_Default_1.jpg"
    />
    <div class="cover" style="opacity: 1"></div>
    <div class="title" style="transform: scale(1)">
      <h1 id="titleText">14<span>:</span>10</h1>
    </div>
  </div>
</template>

<script lang="ts">
</script>

<style lang="scss" scoped>
@import '../assets/public.scss';
.home {
  .bgbox {
    z-index: -3;
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: opacity 1s, transform 0.25s, filter 0.25s;
    backface-visibility: hidden;
  }
  .cover {
    z-index: -1;
    opacity: 0;
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-image: radial-gradient(
        rgba(0, 0, 0, 0) 0%,
        rgba(0, 0, 0, 0.5) 100%
      ),
      radial-gradient(rgba(0, 0, 0, 0) 33%, rgba(0, 0, 0, 0.3) 166%);
    transition: 0.25s;
  }
  .title {
    position: fixed;
    left: 50%;
    top: calc(115px);
    margin-left: -50px;
    width: 100px;
    text-align: center;
    transition: 0.25s;
    #titleText {
      color: white;
      font-weight: inherit;
      text-shadow: 0 0 20px rgb(0 0 0 / 35%);
      cursor: pointer;
      transition: 0.25s;
      line-height: 20px;
      animation-name: delayedFadeIn;
      animation-duration: 2s;
      animation-iteration-count: 1;
      animation-delay: 0s;
    }
  }
}
</style>
