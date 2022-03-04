<template>
  
   <div class="backdrop" @click="closeModal">
       <div class="modal" :class= " { sale:theme ==='sale' } "> 
           <!-- <h2>{{ title }}</h2>
           <p>{{ text }}</p> -->
        <slot> default content</slot>
                <div class="actions">
                <slot name="links"></slot>
                </div>
               

          
       </div>
   </div>
  
</template>


<script>
export default {
    name: 'CliProjectMain',

    props: ['title','text','theme','description'],
    data() {
        return {
              name :'My first Vue app :)',
        };
    },
    methods:{
        closeModal(){
            this.$emit('close');
        }
    }

};
</script>

<style>
.backdrop{
    position:fixed;
    top:10%;
    width:100%;
    height: 100%;
   background: rgba(0,0,0,0.5)
}
.modal{
    width: 400px;
    padding: 40px;
    background: rgb(3, 2, 2);
    border-radius: 10px;
    margin: 100px auto;
    color: white
}

.modal h2{
    color:aqua;
    font-size: 26px;
    font-weight: bold;
    text-transform: uppercase
}


.modal.sale{
    background: crimson;
    color: white;
}
.modal.sale h2{
    color:white
}


a {
    padding: 13px;
    background: white;
    display: inline-block;
    margin: 11px;
    text-decoration: none;
    font-size: 23px;
}

</style>