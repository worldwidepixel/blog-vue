<template>

    <title> Blog - WorldWidePixel </title>
  
    <spacer />
  
    <contentContainer class="contentContainer">
  
      <titleElement> Welcome to my blog. </titleElement>
  
      <div class="welcomeText"> 
  
        Whether it is a long-form thought, or just a quick post, I hope to make this a space I can call my own.
        
      </div>
  
      <div class="latestpost">
  
        <span class="latestTitle"> Latest Post </span>
  
      </div>
  
      <NuxtLink to="/post/test-post">test post</NuxtLink>
  
    </contentContainer>
  
  </template>
  
  <script setup lang="ts">
  const route = useRoute()
  
  // When accessing /posts/1, route.params.id will be 1
  console.log(route.params.slug)
  </script>
  
  <style>
  
    .welcome {
      font-size: 2rem;
      font-weight: bolder;
    }
  
    .contentContainer {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }
  
    .latestPost {
      background-color: #e5e7eb;
    }
  
    .latestTitle {
      font-size: 1.5rem;
      font-weight: bolder;
      color: var(--colour-title-text)
    }
  
  </style>