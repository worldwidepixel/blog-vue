<template>

    <NuxtLayout>
        <NuxtPage />
    </NuxtLayout>

</template>

<style>

@media (max-width: 351px) {
        .desktop {
            display: none;
        }
        .mobile {
            display: none;
        }
        .desktopMobile {
            display: none;
        }
    }
    @media (min-width: 351px) and (max-width: 550px) {
        .desktop {
            display: none;
        }
        .tiny {
            display: none;
        }
    }

    @media (min-width: 551px) {
        .mobile {
            display: none;
        }
        .tiny {
            display: none;
        }
        .mobileTiny {
            display: none;
        }
    }

</style>