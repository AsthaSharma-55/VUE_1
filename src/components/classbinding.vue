<template>
<h1 :class="{green:colorfull}">Class component</h1>
<button v-on:click="colorfull=!colorfull">toggle</button>
</template>

<script>
export default{
    name:"classbinding",
    data(){
        return{
            colorfull:true
        }
    }
}

</script>

<style scoped>
.green{
    background-color: pink;
}
</style>