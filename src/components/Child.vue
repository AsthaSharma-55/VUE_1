<template>
<!-- <h1>{{name}}</h1>
<h1> name is :{{user.name}} email is: {{user.email}}</h1>
<button v-on:click="getdata()" >call function</button> -->
<h1>{{data}}</h1>
<slot></slot>

<!-- <h1>{{data.email}}</h1> -->

</template>

<script>
export default {
    name:'Child',
    props:{
        name:String,
        user:Object,
        getdata:Function,
        data:Object
    }
}
</script>