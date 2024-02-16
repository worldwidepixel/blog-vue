<template>

  <title> WorldWidePixel - Welcome </title>

    <canvas id="static-gradient"></canvas>

    <spacer />

    <div class="mainLayout">

      <div class="mainContent">

        <pixelWordMark class="wordmark" />

        <SubTitleElement style="text-align: center;" class="landingSubtitle">I make things. On the internet.</SubTitleElement>

        <spacer />

        <div class="socialRow">
        
          <NuxtLink to="https://youtube.com/@worldwidepixel"> <LucideYoutube class="whiteIcon" /> </NuxtLink>
          <Bullet />
          <NuxtLink to="https://mastodon.social/@worldwidepixel"> <LucideMessageCircle class="whiteIcon" /> </NuxtLink>
          <Bullet />
          <NuxtLink to="https://bsky.app/profile/worldwidepixel.ca"> <LucideCloud class="whiteIcon" /> </NuxtLink>

        </div>

        <div class="socialRow">
        
        <NuxtLink to="https://projects.worldwidepixel.ca"> <LucideFlaskConical class="whiteIcon" /> </NuxtLink>
        <Bullet />
        <NuxtLink to="https://github.com/worldwidepixel"> <LucideGithub class="whiteIcon" /> </NuxtLink>

      </div>

      </div>

    </div>

</template>

<script setup lang="ts">
const route = useRoute()

// When accessing /posts/1, route.params.id will be 1
console.log(route.params.slug)


definePageMeta({
  layout: 'landing'
})

useSeoMeta({
  ogTitle: "WorldWidePixel - Welcome",
  ogDescription: "I make things. On the internet.",
  title: 'WorldWidePixel - Welcome',
  description: 'I make things. On the internet.',
  ogImage: '~/assets/logo.png',
});

</script>

<style>

  :root {
    --logotype-fill: white;
  }

  .socialRow {
    display: flex;
    flex-direction: row;
    gap: 2rem;
    align-items: center;
    color: white;
  }

  .whiteIcon {
    color: white;
    width: 3rem;
    height: 3rem;
    stroke-width: 2px;
    transition-duration: 0.4s;
  }

  .whiteIcon:active {
    transform: scale(0.9);
  }

  .wordmark {
    height: 4.5rem;
  }

  .mainLayout {
    display: flex;
    flex-direction: row;
    gap: 1rem;
    justify-content: flex-end;
    width: 100%;
    height: calc(100vh - 8rem);
  }

  .mainContent {
    padding: 1rem;
    gap: 2rem;

    background: rgba(0, 0, 0, 0.5);
    backdrop-filter: blur(20px);

    border-radius: 1rem;
    border-bottom-left-radius: 0;
    border-bottom-right-radius: 0;

    -webkit-box-shadow: 0px 0px 20px 5px rgba(0,0,0,0.1);
    box-shadow: 0px 0px 20px 5px rgba(0,0,0,0.1);

    width: fit-content;
    height: 100%;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

/* ACTUAL MOBILE */
  @media (max-width: 675px) {

    .subtitle.desktopMobile {
      font-size: 5vw;
      text-align: center;
    }
    .subtitleTiny.tiny {
      font-size: 5vw;
    }

    .bullet {
      font-size: 5vw;
    }

    .whiteIcon {
    color: white;
    width: 8vw;
    height: 8vw;
    stroke-width: 2px;
    transition-duration: 0.4s;
    }

    .whiteIcon:active {
      transform: scale(0.9);
    }
    .wordmark {
      height: 10vw;
    }
    /* MAIN CONTENT MOBILE */
    .mainContent {
    padding: 1rem;
    gap: 2rem;

    background: rgba(0, 0, 0, 0.5);
    backdrop-filter: blur(20px);

    border-radius: 1rem;
    border-bottom-left-radius: 0;
    border-bottom-right-radius: 0;

    -webkit-box-shadow: 0px 0px 20px 5px rgba(0,0,0,0.1);
    box-shadow: 0px 0px 20px 5px rgba(0,0,0,0.1);

    width: 100%;
    height: 100%;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
    /* MAIN CONTENT MOBILE DEFINITIONS */

  .mainContent * {
    width: fit-content;
  }
  /* MAIN LAYOUT MOBILE */

  .mainLayout {
    display: flex;
    flex-direction: row;
    gap: 1rem;
    justify-content: center;
    width: 100%;
    height: calc(100vh - 8rem);
    padding-right: 1rem;
  }
  }
    /* LITTLE DESKTOPS */
  @media (min-width: 676px) and (max-width: 1300px) {
    /* MAIN CONTENT FOR SMALL DESKTOP */
    .mainContent {
    padding: 1rem;
    gap: 2rem;

    background: rgba(0, 0, 0, 0.5);
    backdrop-filter: blur(20px);

    border-radius: 1rem;
    border-bottom-left-radius: 0;
    border-bottom-right-radius: 0;

    -webkit-box-shadow: 0px 0px 20px 5px rgba(0,0,0,0.1);
    box-shadow: 0px 0px 20px 5px rgba(0,0,0,0.1);

    width: 100%;
    height: 100%;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  /* BIG MONITORS */
  }
  @media (min-width: 1301px) {
    /* MAIN CONTENT FOR LARGE DESKTOP */
    .mainContent {
    padding: 1rem;
    gap: 2rem;

    background: rgba(0, 0, 0, 0.5);
    backdrop-filter: blur(20px);

    border-radius: 1rem;
    border-bottom-left-radius: 0;
    border-bottom-right-radius: 0;

    -webkit-box-shadow: 0px 0px 20px 5px rgba(0,0,0,0.1);
    box-shadow: 0px 0px 20px 5px rgba(0,0,0,0.1);

    width: fit-content;
    height: 100%;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  }

  canvas {
    position: absolute;
    top: 0;
    left: 0;
    z-index: -1;
  }

  #gradient-canvas {
        width:100%;
        height:100%;
        --gradient-color-1: #8e80ff;
        --gradient-color-2: #6ec3f4;
        --gradient-color-3: #fc38ff;
        --gradient-color-4: #b9beff;
  }

  #static-gradient {

    width: 100%;
    height: 100%;

    background-color:hsla(290,100%,75%,1);
    background-image:
    radial-gradient(at 40% 20%, hsla(246,100%,75%,1) 0px, transparent 50%),
    radial-gradient(at 0% 100%, hsla(201,85%,69%,1) 0px, transparent 50%),
    radial-gradient(at 80% 100%, hsla(299,100%,60%,1) 0px, transparent 50%),
    radial-gradient(at 0% 0%, hsla(235,100%,86%,1) 0px, transparent 50%);
  }

  .welcome {
    font-size: 2rem;
    font-weight: bolder;
  }

  .contentContainer {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .latestPost {
    background-color: #e5e7eb;
  }

  .latestTitle {
    font-size: 1.5rem;
    font-weight: bolder;
    color: var(--colour-title-text)
  }

</style>