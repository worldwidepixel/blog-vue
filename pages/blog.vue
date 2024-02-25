<template>

    <title> Blog - WorldWidePixel </title>
  
    <spacer />

    <div class="pageFlex">
  
      <contentContainer class="contentContainer">
  
        <titleElement> Welcome to my blog. </titleElement>
  
        <div class="welcomeText"> 
  
         <SubTitleElement>Whether it is a long-form thought, or just a quick post, I hope to make this a space I can call my own.</SubTitleElement>
        
        </div>
  
       <div class="latestpost">
  
          <span class="latestTitle"> Latest Post </span>
  
        </div>
  
        <NuxtLink to="/post/test-post">test post</NuxtLink>

        <!--<UBlogPost
            v-for="(post, index) in posts"
            :key="index"
            :to="post._path"
            :title="post.title"
            :description="post.description"
            :image="post.image"
            :date="new Date(post.date).toLocaleDateString('en', { year: 'numeric', month: 'short', day: 'numeric' })"
            :authors="post.authors"
            :badge="post.badge"
            :orientation="index === 0 ? 'horizontal' : 'vertical'"
            :class="[index === 0 && 'col-span-full']"
            :ui="{
              description: 'line-clamp-2',
            }"
          />-->
  
      </contentContainer>

    </div>
  
  </template>
  
  <script setup lang="ts">

  import type { BlogPost } from "~/types";

  const { data: page } = await useAsyncData("blog", () => queryContent("/post").findOne());
  if (!page.value) {
    throw createError({ statusCode: 404, statusMessage: "Page not found", fatal: true });
  }

  const { data: posts } = await useAsyncData("posts", () => queryContent<BlogPost>("/post").where({ _extension: "md" }).sort({ date: -1 }).find());


  useSeoMeta({
    ogTitle: "WorldWidePixel - Blog",
    ogDescription: "I make things. On the internet.",
    title: 'WorldWidePixel - Blog',
    description: 'I make things. On the internet.',
    ogImage: '~/assets/logo.png',
  });

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