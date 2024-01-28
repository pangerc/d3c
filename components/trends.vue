<template>
  <div class="themes-bg py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <p
        class="mt-q text-2xl font-bold tracking-tight text-crypto-green sm:text-4xl font-gellix uppercase mb-1 text-center"
      >
        Emerging Macro Themes
      </p>
      <p
        class="mt-1 mb-8 text-lg font-light leading-7 text-gray-500 text-center"
      >
        Identified in the current market cycle (2022 - 2026).
      </p>
      <div
        v-for="(trend, index) in trends"
        :key="trend.headline"
        class="relative pl-9"
      >
        <dt
          class="font-gellix text-gray-200 uppercase text-xl font-light text-center sm:text-3xl py-4 hover:text-4xl"
        >
          <span class="text-crypto-green font-bold">0{{ index + 1 }}</span>
          {{ trend.headline }}
        </dt>
      </div>
    </div>
  </div>
</template>

<script setup>
const trends = [
  {
    id: 1,
    headline: "Multi-asset investing universe",
  },
  {
    id: 2,
    headline: "Smart Contact Platform",
  },
  {
    id: 3,
    headline: "On-chain financial products",
  },
  {
    id: 4,
    headline: "Proof-of-Stake",
  },
  {
    id: 5,
    headline: "Layer-2 scaling",
  },
];
</script>
<style>
.themes-bg {
  background-image: url('/img/themes.png');
  background-size: cover;
}
</style>
