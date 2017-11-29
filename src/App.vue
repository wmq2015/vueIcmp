<template>
    <div id="app">
        <router-view/>
    </div>
</template>

<script>
    export default {
        name: 'app'
    }
</script>

<style>
    html,body{
        height: 100%;
    }
    body,p{
        margin: 0;
        padding: 0;
    }
    #app{
        height: 100%;
    }
    #app > section.el-container:first-child{
        height: 100%;
    }
</style>
