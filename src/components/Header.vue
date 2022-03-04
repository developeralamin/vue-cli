<template>
    <div>
        <h1>{{ user }}</h1>
        <h3>{{ text }}</h3>
        <h3>{{ title }}</h3>
        <h3>{{ address }}</h3>
    </div>
</template>

<script>
export default {
    name: 'CliProjectMain',

    props: ['title','text','address'],
    data() {
        return {
           user:'Rahihan' 
        };
    }

};
</script>

<style>
 h1{
     color: black;
     text-align:center
 }

</style>