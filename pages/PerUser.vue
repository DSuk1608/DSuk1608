<template>
  <div>
    <h2>Word een per user pagina wie ingelofd is </h2>
    <div v-for="lang in programlang" :key="lang">
      <div class="flex justify-between mb-1">
        <span class="text-base font-medium text-blue-700 dark:text-white">{{ lang.name }}</span>
        <span class="text-sm font-medium text-blue-700 dark:text-white">{{lang.width}}%</span>
      </div>
      <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
        <div class="bg-blue-600 h-2.5 rounded-full" style="width:50%"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "PerUser",
  data() {
    return {
      programlang: [
        {name: 'PHP', width:'55'},
        {name: 'Javascript',width:'90'},
        {name: 'Vue.js',width:'75'},
        {name: 'React.js', width:'30'},
      ]
    }
  }

}
</script>

<style scoped>

</style>
