<template>

    <div class="footer">

        <div class="column">

            <span class="aboveTitle">created by</span>
            <span class="footerMain">WorldWidePixel. </span>

        </div>
        
        <squareDivider class="squareDivider" />

        <div class="column">
            <NuxtLink class="footerLink" to="https://youtube.com/@worldwidepixel"> <socialChip> <LucidePlaySquare style="stroke-width: 1px;" /> Youtube </socialChip> </NuxtLink>
            <NuxtLink class="footerLink" to="https://github.com/worldwidepixel"> <socialChip> <LucideGithub style="stroke-width: 1px;" /> Github </socialChip> </NuxtLink>
            <NuxtLink class="footerLink" to="https://bsky.app/profile/worldwidepixel.ca"> <socialChip> <LucideCloud style="stroke-width: 1px;" /> Bluesky </socialChip> </NuxtLink>
        </div>

    </div>

</template>

<style>

    .aboveTitle {
        font-size: 1.25rem;
    }

    .footer {
        background-color: #e7deff;
        height: fit-content;
        width: 100% - 1rem;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        padding: 1rem;
        gap: 2rem;
    }

    .column {
        display: flex;
        flex-direction: column;
        gap: 0.1rem;
        justify-content: flex-start;
    }

    .footerMain {
        color: rgb(0, 0, 0);
        font-size: 2rem;
        font-weight: bolder;
    }

    .social:hover {
        background-color: rgba(0, 0, 0, 0.04);
    }

    .footerLink {
        color: black;
        text-decoration: none;
    }

    .squareDivider {
        background-color: black !important;
    }

</style>