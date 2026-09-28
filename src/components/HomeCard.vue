<script setup lang="ts">
  import type { Component } from 'vue';

  withDefaults(
    defineProps<{
      /** 图标组件，例如从 `@lucide/vue` 导入的图标 */
      icon: Component;
      /** 卡片标题 */
      title: string;
      /** 卡片描述 */
      description?: string;
      /** 可选链接地址，传入后整行可点击 */
      href?: string;
    }>(),
    {
      description: '',
      href: undefined,
    },
  );
</script>

<template>
  <component
    :is="href ? 'a' : 'div'"
    :href="href"
    :target="href ? '_blank' : undefined"
    :rel="href ? 'noopener noreferrer' : undefined"
    class="px-4 w-96 flex gap-3 items-center"
    :class="href ? 'transition-colors hover:bg-accent rounded-md' : ''"
  >
    <component :is="icon" class="text-2xl shrink-0" />
    <div class="flex flex-col">
      <div class="text-xl font-bold">{{ title }}</div>
      <div class="text-sm text-muted-foreground">{{ description }}</div>
    </div>
  </component>
</template>
