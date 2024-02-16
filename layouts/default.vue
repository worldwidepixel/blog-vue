<template>

    <div class="mainPage">

      <navBar />

      <slot />

    </div>

      <pageFooter />

</template>

<style>

@import url(https://fonts.bunny.net/css?family=inter:100,200,300,400,500,600,700,800,900);


:root {
  font-family: Inter, Helvetica, sans-serif;
  /*background-color: #e5e7eb;*/
  background-color: #16181c;
  --colour-foreground: #262a30;
  --colour-text: #c7cbd4;
  --colour-title-text: #ffffff;
  color: #c7cbd4;
}

/*@media (max-width: 351px) {
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
    }*/

.mainPage {
  padding: 1rem;
}

body {
  margin: 0;
}

a {
  color: var(--colour-text);
  text-decoration: underline;
}

</style>