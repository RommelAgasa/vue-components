<template>
  <!-- <GreetUser name="Kyla" />
  <GreetUser name="Rommel" />
  <GreetUser :name="name" /> -->

  <ArticleComponent id="my-article" :title="'Article Title'" :likes="50" :isPublished="true"/>
  
  <!-- <h3>AppComponent username {{ username }}</h3>
  <ComponentC /> -->

  <button @click="showPopup = true">Show Popup</button>
  <PopupComponent v-show="showPopup" @closePopup="closePopup"/>

  <VModelCustomComponents />

  <!-- <CardSlot>Card Content</CardSlot>
  <CardSlot>
    <h2>Card Content</h2>
  </CardSlot>
  <CardSlot>
    <img src="https://picsum.photos/200" alt="">
  </CardSlot>
  <CardSlot></CardSlot> -->

  <CardSlot>
    <template v-slot:header>
      <h3>Header</h3>
    </template>
    <template v-slot:default>
      <img src="https://picsum.photos/200" alt="">
    </template>
    <template v-slot:footer>
      <button>View Details</button>
    </template>
  </CardSlot>



  <SlotProps>
    <template v-slot:default="slotProps">
      <p>First Name: {{  slotProps.firstName }}</p>
      <p>Last Name: {{  slotProps.lastName }}</p>
    </template>
  </SlotProps>


</template>

<script>
// mport GreetUser from './components/Greet.vue'
import ArticleComponent from './components/Article.vue'
// import ComponentC from './components/ComponentC.vue';
import PopupComponent from './components/Popup.vue';
import VModelCustomComponents from './components/VModelCustomComponents.vue';
import CardSlot from './components/CardSlot.vue';
import SlotProps from './components/SlotProps.vue';


export default {
  name: 'App',
  components: {
    // GreetUser,
    ArticleComponent,
    //ComponentC,
    PopupComponent,
    VModelCustomComponents,
    CardSlot,
    SlotProps
  },
  data(){
    return {
      name: 'Rommel',
      showPopup: false
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
  methods: {
    closePopup(name) {
      this.showPopup = false;
      console.log(`Popup closed by ${name}`);
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
