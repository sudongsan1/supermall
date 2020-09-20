<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png">
        <HelloWorld msg="Welcome to Your Vue.js App"/>

        <el-row>
            <el-button>默认按钮</el-button>
            <el-button type="primary">主要按钮</el-button>
            <el-button type="success">成功按钮</el-button>
            <el-button type="info">信息按钮</el-button>
            <el-button type="warning">警告按钮</el-button>
            <el-button type="danger" @click="popUpDanger">危险按钮</el-button>
        </el-row>

<!--        <Echarts/>-->
        <Echarts1/>
    </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld.vue'

    import Echarts1 from "./components/Echarts1";

    export default {
        name: 'App',
        components: {
            HelloWorld,
            //Echarts,
            Echarts1

        },
        methods: {
            popUpDanger() {
                this.$message.error('错了哦，这是一条错误消息');
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
