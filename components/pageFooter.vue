<template>

    <div class="footer">

        <div class="column desktopMobile">

            <span class="aboveTitle desktop">created by</span>
            <span class="footerMain desktop">WorldWidePixel. </span>
            <logo class="footerLogo mobile" />

        </div>
        
        <squareDivider class="squareDivider desktop" />
        <squareDivider class="squareDivider mobile" />


        <div class="column">
            <NuxtLink class="footerLink" to="https://youtube.com/@worldwidepixel"> <socialChip> <LucidePlaySquare style="stroke-width: 1px;" /> Youtube </socialChip> </NuxtLink>
            <NuxtLink class="footerLink" to="https://github.com/worldwidepixel"> <socialChip> <LucideGithub style="stroke-width: 1px;" /> Github </socialChip> </NuxtLink>
            <NuxtLink class="footerLink" to="https://bsky.app/profile/worldwidepixel.ca"> <socialChip> <LucideCloud style="stroke-width: 1px;" /> Bluesky </socialChip> </NuxtLink>
        </div>

    </div>

</template>

<style>

    .footerLogo {
        height: 3rem;
        width: 3rem;
    }

    .aboveTitle {
        font-size: 1.25rem;
    }

    .footer {
        /*background-color: #e7deff;*/
        border-top: solid 2.5px #d7c8ff;
        background-color: #041d30;
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
        color: var(--colour-title-text);
        font-size: 2rem;
        font-weight: bolder;
    }

    .social:hover {
        background-color: rgba(255, 255, 255, 0.04);
    }

    .footerLink {
        color: black;
        text-decoration: none;
    }

    .squareDivider {
        background-color: #28cbd4 !important;
    }

</style>