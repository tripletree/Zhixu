<script setup lang="ts">
import { ArrowRight } from 'lucide-vue-next'
import Reveal from './ui/Reveal.vue'
import BrandMark from './ui/BrandMark.vue'

const links = [
  { label: '系统框架', href: '#framework' },
  { label: '功能矩阵', href: '#features' },
  { label: '业务场景', href: '#scenarios' },
]
</script>

<template>
  <!-- Conversion CTA -->
  <section id="demo" class="relative overflow-hidden border-t border-bone/[0.06]">
    <div class="pointer-events-none absolute inset-0 bg-grid opacity-30" />
    <div
      class="pointer-events-none absolute left-1/2 top-0 size-[40rem] -translate-x-1/2 -translate-y-1/3 rounded-full opacity-50 blur-3xl"
      style="background: radial-gradient(circle, rgba(87, 184, 212, 0.16), transparent 65%)"
    />
    <div
      class="pointer-events-none absolute bottom-0 left-1/4 size-[26rem] rounded-full opacity-40 blur-3xl"
      style="background: radial-gradient(circle, rgba(201, 173, 124, 0.12), transparent 65%)"
    />

    <div class="relative mx-auto max-w-4xl px-6 py-16 text-center lg:py-20">
      <Reveal :y="16">
        <span class="eyebrow text-azure">Let's talk · 预约演示</span>
      </Reveal>
      <Reveal :y="24" :delay="0.08">
        <h2 class="mx-auto mt-6 max-w-3xl text-balance text-4xl font-bold leading-[1.18] tracking-tight text-bone sm:text-5xl">
          与知序一起，让每一次决策更有据可循
        </h2>
      </Reveal>
      <Reveal :y="24" :delay="0.16">
        <p class="mx-auto mt-6 max-w-xl text-[15px] leading-relaxed text-bone-dim">
          让时尚判断成为可验证的 AI 决策。预约一次产品演示，看见数据智能如何融入你的产品开发与提案流程。
        </p>
      </Reveal>
      <Reveal :y="24" :delay="0.24">
        <div class="mt-10 flex justify-center">
          <a
            href="mailto:contact@fabricmind.ai?subject=预约知序%20FabricMind%20产品演示"
            class="group inline-flex items-center gap-2.5 rounded-full bg-bone px-8 py-4 text-[15px] font-medium tracking-wide text-ink-950 transition-all hover:bg-white hover:shadow-[0_0_44px_-8px_rgba(236,234,225,0.45)]"
          >
            预约产品演示
            <ArrowRight class="size-4 transition-transform group-hover:translate-x-1" />
          </a>
        </div>
      </Reveal>
    </div>
  </section>

  <!-- Footer -->
  <footer class="border-t border-bone/[0.06] bg-ink-950">
    <div class="mx-auto max-w-7xl px-6 py-14 lg:px-10">
      <div class="flex flex-col justify-between gap-10 md:flex-row md:items-start">
        <div class="max-w-xs">
          <div class="flex items-center gap-3">
            <BrandMark :size="32" />
            <span class="flex items-baseline gap-2 leading-none">
              <span class="text-[15px] font-medium tracking-wide text-bone">知序</span>
              <span class="font-display text-[15px] italic tracking-wide text-bone-soft">FabricMind</span>
            </span>
          </div>
          <p class="mt-4 text-[13px] leading-relaxed text-bone-dim">
            面向纺织产品开发的智能决策系统。<br />
            AI Decision Intelligence for Fashion and Textile Product Development.
          </p>
        </div>

        <div class="flex gap-16">
          <div>
            <h4 class="eyebrow text-bone-dim">产品</h4>
            <ul class="mt-4 space-y-2.5">
              <li v-for="link in links" :key="link.href">
                <a :href="link.href" class="text-[13px] text-bone-soft transition-colors hover:text-bone">{{ link.label }}</a>
              </li>
            </ul>
          </div>
          <div>
            <h4 class="eyebrow text-bone-dim">联系</h4>
            <ul class="mt-4 space-y-2.5">
              <li>
                <a href="#demo" class="text-[13px] text-bone-soft transition-colors hover:text-bone">预约演示</a>
              </li>
              <li>
                <a href="mailto:contact@fabricmind.ai" class="text-[13px] text-bone-soft transition-colors hover:text-bone">商务咨询</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <!-- Compliance bar -->
    <div class="border-t border-bone/[0.06]">
      <div
        class="mx-auto flex max-w-7xl flex-col items-center justify-between gap-2 px-6 py-5 text-[12px] text-mist sm:flex-row lg:px-10"
      >
        <span>© 2026 知序 FabricMind，保留所有权利.</span>
        <a
          href="https://beian.miit.gov.cn"
          target="_blank"
          rel="noopener noreferrer"
          class="transition-colors hover:text-bone-soft"
        >
          京ICP备10009259号
        </a>
      </div>
    </div>
  </footer>
</template>
