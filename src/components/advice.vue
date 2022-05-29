<template>
  <div class="advice">
    <hr>
    <div class="advice_title">
      {{ title }}
    </div>
    <hr>
    <div class="advice_text" v-html="text">
    </div>
  </div>
</template>

<script>

export default {
  name: 'adviceVue',
  props: ['title', 'text'],
};
</script>

<style lang="scss" scoped>

</style>
