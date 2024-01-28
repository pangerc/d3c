<template>
  <div class="bg-white py-16 sm:py-24">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div
        class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-3"
      >
        <div>
          <p
            class="mt-q text-2xl font-bold tracking-tight text-crypto-green sm:text-4xl font-gellix uppercase mb-2"
          >Category Pioneers
          </p>
          <p class="mt-1 text-lg font-light leading-7 text-gray-700">
            We’re already the earliest investors in the emerging category leaders of the current macro narratives.
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
            <dt class="font-gellix font-semibold text-gray-800 uppercase">
              <span class="text-crypto-green font-bold">0{{ index + 1 }}</span>
              {{ category.name }}
            </dt>
            <dd class="mt-2 ">
              <img :src="'/img/'+category.investment" class="h-12 ml-6 opacity-30 hover:opacity-90">
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
    investment:
      "babylon.png",
  },
  {
    name: "DECENTRALIZED EXCHANGE",
    investment:
      "satory.png",
  },
  {
    name: "Restaking",
    investment:
      "swell.png",
  },
  {
    name: "Cryptography",
    investment:
      "cubist.png",
  },  
  {
    name: "Web3 AI",
    investment:
      "hyperoracle.png",
  },
  {
    name: "Intent / Tradfi",
    investment:
      "lifi.png",
  },  
  {
    name: "Advanced Defi",
    investment:
      "soon4.svg",
  },
  {
    name: "Real World Assets",
    investment:
      "soon4.svg",
  },
  {
    name: "Consumer",
    investment:
      "soon4.svg",
  },

];
</script>
