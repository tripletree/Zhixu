<script setup lang="ts">
import { onMounted, onUnmounted, ref } from 'vue'
import { ArrowUpRight } from 'lucide-vue-next'
import BrandMark from './ui/BrandMark.vue'

const scrolled = ref(false)
const onScroll = () => {
  scrolled.value = window.scrollY > 24
}
onMounted(() => {
  onScroll()
  window.addEventListener('scroll', onScroll, { passive: true })
})
onUnmounted(() => window.removeEventListener('scroll', onScroll))

const links = [
  { label: '解决方案', href: '#framework' },
  { label: '功能矩阵', href: '#features' },
  { label: '业务场景', href: '#scenarios' },
]
</script>

<template>
  <header
    class="fixed inset-x-0 top-0 z-50 transition-all duration-500"
    :class="scrolled ? 'border-b border-bone/10 bg-ink-950/70 backdrop-blur-xl' : 'border-b border-transparent'"
  >
    <nav class="mx-auto flex h-16 max-w-7xl items-center justify-between px-6 lg:px-10">
      <a href="#top" class="group flex items-center gap-3">
        <BrandMark :size="34" />
        <span class="flex items-baseline gap-2 leading-none">
          <span class="text-[15px] font-medium tracking-wide text-bone">知序</span>
          <span class="font-display text-[15px] italic tracking-wide text-bone-soft">FabricMind</span>
        </span>
      </a>

      <div class="hidden items-center gap-9 md:flex">
        <a
          v-for="link in links"
          :key="link.href"
          :href="link.href"
          class="text-[13px] tracking-wide text-bone-dim transition-colors hover:text-bone"
        >
          {{ link.label }}
        </a>
      </div>

      <a
        href="#demo"
        class="group inline-flex items-center gap-1.5 rounded-full border border-bone/15 bg-bone/[0.03] px-4 py-2 text-[13px] font-medium tracking-wide text-bone transition-all hover:border-azure/40 hover:bg-azure/10"
      >
        预约演示
        <ArrowUpRight class="size-3.5 transition-transform group-hover:translate-x-0.5 group-hover:-translate-y-0.5" />
      </a>
    </nav>
  </header>
</template>
