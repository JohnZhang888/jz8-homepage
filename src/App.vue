<script setup lang="ts">
import { Rss, Vote, Puzzle } from '@lucide/vue';
import HomeCard from '@/components/HomeCard.vue';
import logoLight from '@/assets/logos/logo-light.svg';
import logoDark from '@/assets/logos/logo-dark.svg';
</script>

<template>
  <div class="flex min-h-svh w-full items-center justify-center bg-background px-8">
    <div class="w-full max-w-sm flex flex-col gap-4">
      <div class="px-4">
        <img :src="logoLight" alt="JZ8" class="h-8 w-auto dark:hidden" />
        <img :src="logoDark" alt="JZ8" class="hidden h-8 w-auto dark:block" />
      </div>
      <div class="bg-card rounded-md border py-4 flex flex-col">
        <HomeCard :icon="Rss" title="博客" description="记录日常生活、OI 学习等内容。" href="https://blogs.jz8.de5.net" />
        <HomeCard :icon="Vote" title="EasyVote" description="一个简易的投票与唱票程序。" href="https://ev.jz8.de5.net" />
        <HomeCard :icon="Puzzle" title="Puzzles" description="一个可能有点无聊的网页解谜游戏。" href="https://puzzles.jz8.de5.net" />
      </div>
      <div class="flex flex-col px-4">
        <div class="text-muted-foreground font-bold my-1">友情链接</div>
        <a href="https://cnblogs.com/aeee5x" target="_blank" rel="noopener noreferrer"
          class="text-primary w-fit transition-opacity hover:opacity-70 active:opacity-50 focus-visible:opacity-50">
          AeeE5x（博客园）
        </a>
        <a href="https://commongoldingot.github.io" target="_blank" rel="noopener noreferrer"
          class="text-primary w-fit transition-opacity hover:opacity-70 active:opacity-50 focus-visible:opacity-50">
          CommonGoldIngot
        </a>
      </div>

    </div>
  </div>
</template>
