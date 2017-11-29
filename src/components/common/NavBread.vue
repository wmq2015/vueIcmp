<template>
    <el-tabs v-model="activeName" @tab-click="handleClick">
        <el-tab-pane
        v-for="(item,index) in navNames"
        :label="item"
        :name="item"
        :key="index">
            <slot :name="item"></slot>
        </el-tab-pane>
    </el-tabs>
</template>
<style>

</style>
<script>

    export default {
        props: ['navNames'],
        data() {
            return {
                activeName: this.navNames[0],
            }
        },
        methods: {
            handleClick(tab, event){

            }
        }
    }
</script>
