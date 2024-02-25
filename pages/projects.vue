<template>

    <title> Projects - WorldWidePixel </title>

    <spacer />

    <div class="pageFlex">

    <ContentContainer>

        <titleElement> Projects </titleElement>

        <SubTitleElement>

            Here are some of the projects I've made or are a part of. Hope you enjoy them!

        </SubTitleElement>

        <hr>

        <div class="projectContainer">

            <span class="infoContainer">

                <img class="projectIcon" src="https://projects.worldwidepixel.ca/servify512.png">

                <span class="projectTitle">Serv-ify</span>

            </span>

            <span class="projectDesc">Find Minecraft server info, relatively easily.</span>

            <NuxtLink class="projectButton" to="https://projects.worldwidepixel.ca/servify">Visit Project</NuxtLink>

        </div>

        <div class="projectContainer">

            <span class="infoContainer">

                <img class="projectIcon" src="https://projects.worldwidepixel.ca/nameify512.png">

                <span class="projectTitle">Name-ify</span>

            </span>

            <span class="projectDesc">A simple Minecraft nickname formatting generator.</span>

            <NuxtLink class="projectButton" to="https://projects.worldwidepixel.ca/nameify">Visit Project</NuxtLink>

        </div>

        <div class="projectContainer">

            <span class="infoContainer">

                <img class="projectIcon" src="https://www.imateapot.xyz/favicon.ico">

                <span class="projectTitle">imateapot.xyz</span>

            </span>

            <span class="projectDesc">I am a teapot. Are you?</span>

            <NuxtLink class="projectButton" to="https://imateapot.xyz">Visit Site</NuxtLink>

        </div>

        <div class="projectContainer">

            <span class="infoContainer">

                <img class="projectIcon" src="https://www.loopmc.org/img/icon512.png">

                <span class="projectTitle">Loop</span>

            </span>

            <span class="projectDesc">Improving the Minecraft experience for older versions.</span>

            <NuxtLink class="projectButton" to="https://loopmc.org">Visit Site</NuxtLink>

        </div>

        <div class="projectContainer">

            <span class="infoContainer">

                <img class="projectIcon" src="https://nineminecraft.com/img/9icon.png">

                <span class="projectTitle">nineMinecraft</span>

            </span>

            <span class="projectDesc">A satire 9minecraft clone, and warning site.</span>

            <NuxtLink class="projectButton" to="https://nineminecraft.com">Visit Site</NuxtLink>

        </div>

        <div class="projectContainer">

            <span class="infoContainer">

                <img class="projectIcon" src="https://facts.worldwidepixel.ca/img/icon.png">

                <span class="projectTitle">Minefacts</span>

            </span>

            <span class="projectDesc">One Minecraft fact, every day, for all of 2024.</span>

            <NuxtLink class="projectButton" to="https://facts.worldwidepixel.ca">Visit Site</NuxtLink>

        </div>

        <div class="projectContainer">

            <span class="infoContainer">

                <img class="projectIcon" src="https://raw.githubusercontent.com/worldwidepixel/blueRinth/main/img/icon.png">

                <span class="projectTitle">blueRinth</span>

            </span>

            <span class="projectDesc">Change the colour of Modrinth.</span>

            <NuxtLink class="projectButton" to="https://addons.mozilla.org/firefox/addon/bluerinth/">See on Mozilla Addons</NuxtLink>

        </div>

        <div class="projectContainer">

            <span class="infoContainer">

                <img class="projectIcon" src="https://raw.githubusercontent.com/worldwidepixel/modBar/main/img/icon256.png">

                <span class="projectTitle">modbar</span>

            </span>

            <span class="projectDesc">The easiest way to find your favourite Modrinth projects.</span>

            <NuxtLink class="projectButton" to="https://addons.mozilla.org/firefox/addon/themodbar/">See on Mozilla Addons</NuxtLink>

        </div>

    </ContentContainer>

    </div>

</template>

<style>

    hr {
        width: 100%;
    }

    .projectButton {
        color: var(--colour-title-text);
        background-color: rgba(255, 255, 255, 0.04);
        font-weight: bolder;
        text-decoration: none;
        width: fit-content;
        font-size: 1.25rem;
        padding: 1rem;
        border-radius: 1rem;
        transition-duration: 0.4s;
    }

    .projectButton:active {
        transform: scale(0.9);
    }

    .infoContainer {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 1rem;
        align-items: center;
    }

    .projectIcon {
        height: 3rem;
    }

    .projectContainer {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        background-color: rgba(255, 255, 255, 0.04);
        padding: 1rem;
        border-radius: 0.5rem;
    }

    .projectTitle {
        font-size: 2rem;
        color: var(--colour-title-text);
        font-weight: bolder;
    }

</style>

<script setup lang="ts">
useSeoMeta({
  ogTitle: "WorldWidePixel - Projects",
  ogDescription: "I make things. On the internet.",
  title: 'WorldWidePixel - Projects',
  description: 'I make things. On the internet.',
  ogImage: '~/assets/logo.png',
});
</script>