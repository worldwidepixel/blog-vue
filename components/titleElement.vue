<template>

    <div class="title desktopMobile">

        <slot />

    </div>

    <div class="titleTiny tiny">

        <slot />

    </div>

</template>

<style>

.title {
    font-size: 3rem;
    font-weight: bolder;
    color: var(--colour-title-text);
}

.titleTiny {
    font-size: 1.5rem;
    font-weight: bolder;
    color: var(--colour-title-text);
}

</style>