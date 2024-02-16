<template>

    <div class="subtitle desktopMobile">

        <slot />

    </div>

    <div class="subtitleTiny tiny">

        <slot />

    </div>

</template>

<style>

.subtitle {
    font-size: 1.5rem;
    font-weight: light;
    color: var(--colour-title-text);
}

.subtitleTiny {
    font-size: 1rem;
    font-weight: bold;
    color: var(--colour-title-text);
}

</style>