<template>

    <span class="social"> <slot /> </span>

</template>

<style>

.social {
        display: flex;
        flex-direction: row;
        gap: 0.25rem;
        align-items: center;
        font-size: 1.25rem;
        transition-duration: 0.4s;
        padding: 0.5rem;
        border-radius: 5rem;
        user-select: none;
        width: fit-content;
}

</style>