<template>
  <div class="bg-white py-16 sm:py-24">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div
        class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-3"
      >
        <div>
          <p
            class="mt-q text-2xl font-bold tracking-tight text-crypto-green sm:text-4xl font-gellix uppercase mb-2"
          >
            Mega Theses
          </p>
          <p class="mt-1 text-lg font-light leading-7 text-gray-700">
            DC3 is a thesis-driven Web3 fund, with strong understanding in
            blockchain technology and deep network across the industry.
          </p>
        </div>
        <dl
          class="col-span-2 grid grid-cols-1 gap-x-8 gap-y-10 text-base text-gray-600 sm:grid-cols-2 lg:gap-y-16"
        >
          <div
            v-for="(feature, index) in features"
            :key="feature.name"
            class="relative pl-9"
          >
            <dt class="font-gellix font-semibold text-gray-800 uppercase">
              <span class="text-crypto-green font-bold">0{{ index + 1 }}</span>
              {{ feature.name }}
            </dt>
            <dd class="mt-2 font-gellix text-sm text-gray-500 leading-7">
              {{ feature.description }}
            </dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>

<script setup>
const features = [
  {
    name: "Watershed Moment",
    description:
      "One of the largest wealth transfers in human history is taking place now; various asset classes will be ported onto the blockchains over the next decade. ",
  },
  {
    name: "The Great Unraveling",
    description:
      "Decentralization of data governance and modularization of infrastructure services are the critical technology drivers for Web3 adoption among businesses and users.",
  },
  {
    name: "New architectures",
    description:
      "Careful design of tokenomics enables positive feedback loops in and beyond communities, which ultimately drives higher user engagement and accelerates Web3 mass adoption.",
  },
  {
    name: "Timing is everything",
    description:
      "Investing in Web3 now is similar to investing in commercial Internet in the late 90s and early 00s. The best opportunities in infrastructure investments are unfolding, and innovations in Web3 killer applications are just forming. Early investors usually harvest the highest venture scale returns. ",
  },
];
</script>
