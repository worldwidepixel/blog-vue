<template>

    <nav>

        <div class="navContents">

            <logo />

            <squareDivider />

            <div class="navItem"> <NuxtLink to="https://worldwidepixel.ca">Home</NuxtLink> </div>

            <div class="navItem"> <NuxtLink to="/">Blog</NuxtLink> </div>

            <div class="navItem"> <NuxtLink to="/posts">Posts</NuxtLink> </div>

            <div class="navItem"> <NuxtLink to="/about">About</NuxtLink> </div>

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

    background-color: #ffffff;
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
    color: black;
    text-decoration: none;
}

a {
    text-decoration: none;
}

</style>