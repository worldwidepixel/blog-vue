<script setup lang="ts">
import { withoutTrailingSlash, joinURL } from "ufo";
import type { BlogPost } from "~/types";

const route = useRoute();

const { data: post } = await useAsyncData(route.path, () => queryContent<BlogPost>(route.path).findOne());
if (!post.value) {
  throw createError({ statusCode: 404, statusMessage: "Post not found", fatal: true });
}

const { data: surround } = await useAsyncData(`${route.path}-surround`, () => queryContent("/post").where({ _extension: "md" }).without(["body", "excerpt"]).sort({ date: -1 }).findSurround(withoutTrailingSlash(route.path)), { default: () => [] });

const title = post.value.head?.title || post.value.title;
const description = post.value.head?.description || post.value.description;

useSeoMeta({
  title,
  ogTitle: title,
  description,
  ogDescription: description,
});
</script>

<template>

  <main>

    <div class="pageFlex">

      <spacer />

      <div class="post">

        <ContentRenderer v-if="post && post.body" :value="post" />

      </div>

      <spacer />
    
    </div>

  </main>

</template>

<style>


.pageFlex {
  display: flex;
  align-items: center;
  flex-direction: column;
}

.post {
  background-color: var(--colour-foreground);
  padding: 2rem;
  padding-top: 1rem;
  border-radius: 1rem;
  box-shadow: 0px 0px 10px -3px rgba(0,0,0,0.5);
  max-width: 60rem;
}

h1 {
  color: var(--colour-title-text);
}

h1 a {
  color: var(--colour-title-text);
}

h2 {
  color: var(--colour-title-text);
}

h2 a {
  color: var(--colour-title-text);
}

img {
  max-width: 100%;
  border-radius: 1rem;
}

</style>