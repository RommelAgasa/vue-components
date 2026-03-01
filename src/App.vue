<template>
  <!-- <GreetUser name="Kyla" />
  <GreetUser name="Rommel" />
  <GreetUser :name="name" /> -->

  <ArticleComponent id="my-article" :title="'Article Title'" :likes="50" :isPublished="true"/>
</template>

<script>
// mport GreetUser from './components/Greet.vue'
import ArticleComponent from './components/Article.vue'

export default {
  name: 'App',
  components: {
    // GreetUser,
    ArticleComponent
  },
  data(){
    return {
      name: 'John'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
