<template>
  <div class="recipes">
    <button @click="opened = !opened" class="recipes_title">
      {{ recipe.title }}
    </button>
    <div v-show="opened" class="recipes_content">
      <div class="recipes_text" v-html="recipe.text"></div>
      <div class="recipes_ingredients">
        Для него понадобятся:
        <ul>
          <li v-for="(ingredient, index) in recipe.ingredients" :key="index">
          {{ ingredient }}
          </li>
        </ul>
      </div>
      <div class="recipes_steps">
        Что делать:
        <ol>
          <li v-for="(step, index) in recipe.steps" :key="index">
          {{ step }}
          </li>
        </ol>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'recipesVue',
  props: ['recipe'],
  data: () => ({
    opened: false,
  }),

};

</script>

<style lang="scss" scoped>
  .recipes_title {
    margin-bottom: 10px;
    text-align: left;
    font-size: 20px;
    width: 100%;
  }
</style>
