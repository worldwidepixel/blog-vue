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
  background-color: #e5e7eb;
}

.mainPage {
  padding: 1rem;
}

body {
  margin: 0;
}

</style>