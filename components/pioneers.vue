<template>
  <div class="themes-bg py-16 sm:py-24">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div
        class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-3"
      >
        <div>
          <p
            class="mt-q text-2xl font-bold tracking-tight text-crypto-green sm:text-4xl font-gellix uppercase mb-2"
          >
            Category Pioneers
          </p>
          <p class="mt-1 text-lg font-light leading-7 text-gray-200">
            We’re already the earliest investors in the emerging category
            leaders of the current macro narratives.
          </p>
        </div>
        <dl
          class="col-span-2 grid grid-cols-1 gap-x-8 gap-y-6 text-base text-gray-600 sm:grid-cols-2 lg:gap-y-12"
        >
          <div
            v-for="(category, index) in categories"
            :key="category.name"
            class="relative pl-9"
          >
            <dt class="font-gellix font-semibold text-gray-300 uppercase">
              <span class="text-crypto-green font-bold">0{{ index + 1 }}</span>
              {{ category.name }}
            </dt>
            <dd class="mt-2">
              <template v-if="category.investments">
                <a
                  v-for="investment in category.investments"
                  :key="investment.image"
                  :href="investment.url"
                  target="_blank"
                >
                  <img
                    :src="'/img/' + investment.image"
                    :class="investment.size"
                    :alt="investment.company"
                    class="ml-6 opacity-70 hover:opacity-90 mt-8"
                  />
                </a>
              </template>
              <div
                v-else
                class="text-crypto-green uppercase mt-3 pl-6 text-xl font-light"
              >
                soon
              </div>
            </dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>

<script setup>
const categories = [
  {
    name: "BTC 2.0",
    investments: [
      {
        image: "babylon-white.svg",
        company: "Babylon",
        url: "http://babylonchain.io",
        size: "h-7",
      },
      {
        image: "bitmaptech-white.svg",
        company: "Bitmap Tech",
        url: "https://bitmap.tech",
        size: "h-8",
      },
    ],
  },
  {
    name: "DECENTRALIZED EXCHANGE",
    investments: [
      {
        image: "satori2.svg",
        company: "Satori",
        url: "https://satori.finance",
        size: "h-7",
      },
    ],
  },
  {
    name: "Restaking",
    investments: [
      {
        image: "swell.svg",
        company: "Swell",
        url: "http://swellnetwork.io/",
        size: "h-12",
      },
    ],
  },
  {
    name: "Cryptography",
    investments: [
      {
        image: "cubist2.svg",
        company: "Cubist",
        url: "https://cubist.dev",
        size: "h-6",
      },
    ],
  },
  {
    name: "Web3 AI",
    investments: [
      {
        image: "ho.svg",
        company: "Hyperoracle",
        url: "http://hyperoracle.io",
        size: "h-14",
      },
    ],
  },
  {
    name: "Real World Assets",
    investments: [
      {
        image: "plume.svg",
        company: "Plume",
        url: "http://plumenetwork.xyz",
        size: "h-10",
      },
    ],
  },
  {
    name: "Intent / Tradfi",
  },
  {
    name: "Advanced Defi",
  },
  {
    name: "Consumer",
  },
];
</script>
<style>
.themes-bg {
  background-image: url("/img/themes.png");
  background-size: cover;
}
</style>
