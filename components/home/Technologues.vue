<template>
  <div class="max-w-7xl mx-auto border-l border-r border-dashed border-gray-700 pt-4 pb-6 px-4">
    <div class="max-w-prose text-center mx-auto pb-4">
      <p class="text-xs leading-6 text-indigo-600 font-semibold tracking-wide lowercase">{{ $t('technologies.subtext') }}</p>
      <div v-if="$config.social.linkedin">
        <a :href="`https://linkedin.com/in/${$config.social.linkedin}`" target="_blank" rel="noreferrer" class="mt-2 text-3xl hover:text-hot-pink leading-8 font-extrabold tracking-tight text-gray-500">{{ $t('technologies.header') }}</a>
      </div>
      <div v-else>
        <div class="mt-2 text-3xl hover:text-hot-pink leading-8 font-extrabold tracking-tight text-gray-500">{{ $t('technologies.header') }}</div>
      </div>
    </div>
    <div class="grid grid-cols-1 gap-4 sm:grid-cols-6">
      <div v-for="(rec, index) in $config.technologies.meta" :key="`rec-${index}`" class="relative h-full bg-gray-900 rounded-lg shadow-lg text-base w-full">
        <div class="rounded-t-lg px-5 py-5 sm:px-8 sm:py-8y">
          <div class="grid grid-cols-1">
            <div class="text-center text-gray-400 font-semibold py-2">
              <strong class="text-gray-200 font-semibold">{{ rec.name }}</strong>
            </div>
            <div class="flex-shrink-0 transition duration-500 ease-in-out transform hover:-translate-y-1 hover:scale-110">
              <img class="mx-auto w-25 h-25 py-5 px-5" :src="rec.image" alt="Varun">
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  methods: {
  }
}
</script>

<style scoped>

</style>
