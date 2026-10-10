<script setup lang="ts">
  import { Rss, Vote, Puzzle } from '@lucide/vue';
  import HomeCard from '@/components/HomeCard.vue';
</script>

<template>
  <div class="flex min-h-svh w-full items-center justify-center bg-secondary">
    <div class="block">
      <div class="text-2xl font-bold pl-4">JZ8</div>
      <div class="bg-card rounded-md border mt-2 py-4 flex flex-col">
        <HomeCard
          :icon="Rss"
          title="博客"
          description="记录日常生活、OI 学习等内容。"
          href="https://blogs.jz8.de5.net"
        />
        <HomeCard
          :icon="Vote"
          title="EasyVote"
          description="一个简易的投票与唱票程序。"
          href="https://ev.jz8.de5.net"
        />
        <HomeCard
          :icon="Puzzle"
          title="Puzzles"
          description="一个可能有点无聊的网页解谜游戏。"
          href="https://puzzles.jz8.de5.net"
        />
      </div>
    </div>
  </div>
</template>
