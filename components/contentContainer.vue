<template>

    <div class="contentContainer">

        <slot />
    
    </div>

</template>

<style>

    .contentContainer {
        border-radius: 1rem;
        /*background-color: white;*/
        background-color: var(--colour-foreground);
        padding: 2rem;
        box-shadow: 0px 0px 10px -3px rgba(0,0,0,0.5);
        max-width: 60rem;
    }

</style>