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
    class="px-4 w-full flex gap-3 items-center py-2"
    :class="
      href
        ? 'transition-colors hover:bg-foreground/8 focus-visible:bg-foreground/12 active:bg-foreground/12'
        : ''
    "
  >
    <component :is="icon" class="text-2xl shrink-0 text-primary" />
    <div class="flex flex-col">
      <div class="text-xl font-semibold">{{ title }}</div>
      <div class="text-sm text-muted-foreground">{{ description }}</div>
    </div>
  </component>
</template>
