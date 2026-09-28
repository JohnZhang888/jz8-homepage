<script setup lang="ts">
  import { Rss, Vote, Puzzle } from '@lucide/vue';
  import HomeCard from '@/components/HomeCard.vue';
</script>

<template>
  <div class="flex min-h-svh w-full items-center justify-center bg-secondary">
    <div class="block">
      <div class="text-2xl font-bold pl-4">JZ8</div>
      <div class="bg-background rounded-md border-b-card mt-2 py-4 flex flex-col gap-4">
        <HomeCard
          :icon="Rss"
          title="博客"
          description="记录日常生活、OI 学习等内容。"
        />
        <HomeCard
          :icon="Vote"
          title="EasyVote"
          description="一个简易的投票与唱票程序。"
        />
        <HomeCard
          :icon="Puzzle"
          title="Puzzles"
          description="一个可能有点无聊的网页解谜游戏。"
        />
      </div>
    </div>
  </div>
</template>
