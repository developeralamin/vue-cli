<template>

    <div>
       <h1>{{name}}</h1>
       <h1>{{topDesct}}</h1>
       <h2>Welcome to cse </h2>
       <teleport to=".modals" v-if="showModal">
          <Main  :text="text" theme="sale" @close="toggleModal">  

           <template v-slot:links>
             <a href="#">Sign up </a>
             <a href="#">Sign in </a>
          </template>
              <h1>{{ title="This is Props title render her" }}</h1>
            <p>{{ text="This is Props text here" }}</p>
            <p>{{ description="description" }}</p>
          </Main>
       </teleport>

     
      <teleport to=".modals" v-if="showModalTwo">
          <Main  theme="sale" @close="toggleModalTwo">  
              <h1>This is Another heading content</h1>
          <p>This is  Another paragraph content</p>
          </Main>
       </teleport>

       <button id="btn" @click="toggleModal">Open Modal (alt)</button>    
       <button id="btn" @click="toggleModalTwo">Open Modal) </button>    
  
   </div>    
</template>

<script>
import Main from './components/Main.vue';

export default {
  name: 'CliProjectApp',
  components: {
      Main,
    },

  data() {
    return {
    
        name :'My first Vue app :)',
        age:30,
        // address:'dhaka',
        topDesct:"This is title section now",
        description:'Text section now here',
        showModal:false,
        showModalTwo:false
    };
  },
  methods:{
     toggleModal(){
       this.showModal = !this.showModal
     },
     toggleModalTwo(){
        this.showModalTwo = !this.showModalTwo
     }
  }

};
</script>

<style scoped>
#btn{
  text-align: center;
    margin: 0 auto;
    margin-left: 45%;
    margin-top: 2%;
    font-size: 36px;

}
  p{
    font-size: 30px;
  }
  h1{
    text-align: center;
    color: rgb(0, 0, 0);
    font-size: 40px;
  }

</style>