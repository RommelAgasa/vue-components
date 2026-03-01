<template>
  <!-- <GreetUser name="Kyla" />
  <GreetUser name="Rommel" />
  <GreetUser :name="name" /> -->

  <ArticleComponent id="my-article" :title="'Article Title'" :likes="50" :isPublished="true"/>
  
  <h3>AppComponent username {{ username }}</h3>
  <ComponentC />

</template>

<script>
// mport GreetUser from './components/Greet.vue'
import ArticleComponent from './components/Article.vue'
import ComponentC from './components/ComponentC.vue';

export default {
  name: 'App',
  components: {
    // GreetUser,
    ArticleComponent,
    ComponentC
  },
  data(){
    return {
      name: 'Rommel'
    }
  },
  // If property is only utilized in the immediate child component, you can specify provide as a function
  provide() {
    return {
      username: this.name
    }
  },
  // If property is utilized further down the component tree, you can specify provide as an object
  // provide: {
  //   username: 'rommel'
  // }
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
