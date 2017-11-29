<template>
    <el-header>
        <el-menu
            :default-active="activeIndex"
            class="el-menu-demo"
            mode="horizontal"
            background-color="#4d9cd7"
            text-color="#fff"
            active-text-color="#ffd04b"
            @select="handleSelect">
            <el-row type="flex" align="middle">
                <el-col :span="4" style="padding-left: 20px">
                    <router-link to="/">
                        <img src="/static/images/logo.png" alt="logo" style="vertical-align: middle">
                    </router-link>
                </el-col>
                <el-col :span="12">
                    <el-submenu index="1">
                        <template slot="title">云赢营销</template>
                        <el-menu-item index="1-1">云赢网络吧</el-menu-item>
                        <el-menu-item index="1-2">云赢测试号</el-menu-item>
                        <el-menu-item index="1-2">小语薇薇</el-menu-item>
                    </el-submenu>
                </el-col>
                <el-col :span="4" :offset="4" style="text-align: right;padding-right: 20px">
                    <el-dropdown trigger="click">
                        <span class="el-dropdown-link" style="color: #fff">
                            <img src="/static/images/header-pic_03.png" alt="" style="width: 30px;height: 30px;vertical-align: middle">
                            admin
                            <i class="el-icon-arrow-down el-icon--right"></i>
                        </span>
                        <el-dropdown-menu slot="dropdown">
                            <el-dropdown-item>退出登录</el-dropdown-item>
                        </el-dropdown-menu>
                    </el-dropdown>
                </el-col>
            </el-row>
        </el-menu>
    </el-header>
</template>
<style scoped>
    .el-header{
        padding: 0;
    }
</style>
<script>

    export default {
        data() {
            return {
                activeIndex: '1'
            }
        },
        methods: {
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
            }
        }
    }
</script>
