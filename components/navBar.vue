<template>

    <nav>

        <div class="navContents">

            <logo />

            <squareDivider class="desktop" />

            <div class="navItem desktop"> <NuxtLink to="/">Home</NuxtLink> </div>

            <div class="navItem mobileTiny"> <NuxtLink to="/"><LucideHome /></NuxtLink> </div>

            <div class="navItem desktop"> <NuxtLink to="/blog">Blog</NuxtLink> </div>

            <div class="navItem mobileTiny"> <NuxtLink to="/blog"><LucideNotebookPen /></NuxtLink> </div>

            <div class="navItem desktop"> <NuxtLink to="/about">About</NuxtLink> </div>

            <div class="navItem mobileTiny"> <NuxtLink to="/about"><LucideAmpersand /></NuxtLink> </div>

        </div>

    </nav>

</template>

<style>

@import url(https://fonts.bunny.net/css?family=inter:100,200,300,400,500,600,700,800,900);


nav {
    /* padding: 0.5rem; */
    width: (100% - 1rem);

    font-family: 'Inter', sans-serif;

}

.navContents {

    /*background-color: var(--colour-foreground);
    background-color: #262a30;*/
    background-color: rgba(38, 42, 49, 0.75);
    border-radius: 1rem;
    padding: 1rem;
    box-shadow: 0px 0px 10px -3px rgba(0,0,0,0.5);

    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 2rem;
    


}

logo {
    height: 2rem;
}

.navItem {
    font-weight: bolder;
    user-select: none;
    transition-duration: 0.4s;
}

.navItem:active {
    transform: scale(0.9);
}

.navItem a {
    color: var(--colour-text);
    text-decoration: none;
}

a {
    text-decoration: none;
}

</style>