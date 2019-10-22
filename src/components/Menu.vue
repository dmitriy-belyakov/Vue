<template>
    <div id = "Menu">
        <el-menu
            background-color="#545c64"
            text-color="#fff"
            active-text-color="#ffd04b">

            <el-submenu index="1">
                <template slot="title">
                    <span> First </span>
                </template>
                <el-menu-item-group>
                    <el-menu-item index="1-1"> <span> Something </span> </el-menu-item>
                    <el-menu-item index="1-2"> <span> Else </span> </el-menu-item>
                </el-menu-item-group>
            </el-submenu>

            <el-menu-item index="2">
                <span>Second</span>
            </el-menu-item>

            <el-menu-item index="3">
                <span>Third</span>
            </el-menu-item>

            <el-menu-item index="4">
                <span>Fourth</span>
            </el-menu-item>
        </el-menu>
    </div>
</template>

<style scoped>
    @import url("//unpkg.com/element-ui@2.12.0/lib/theme-chalk/index.css");
    #Menu{
        width: 33vh;
        height: 93vh;
        background: #545c64;
        padding: 0;
        margin: 0;
        float: left;
    }
    el-menu{
        width: 90vh;
    }
    span{
        text-shadow: -2px 9px 9px #151216;
        font-size: 1.5em;
    }
    ul{
        border-right: 0px;
    }
</style>
