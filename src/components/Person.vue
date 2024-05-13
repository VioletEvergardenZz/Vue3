<template>
    <!-- html -->
    <div class="person">
        <h2>姓名 {{name}}</h2>
        <h2>年龄 {{age}}</h2>
        <h2>地址 {{address}}</h2>
        <button @click="changeName">修改名字</button>
        <button @click="changeAge">修改年龄</button>
        <button @click="showTel">查看联系事件</button>
    </div>
</template>

<script setup lang="ts" name="Person">
    import { ref } from "vue";

    // 数据 响应式
    let name=ref('xiaoxiao')
    let age=ref(18)
    let tel=13888888888
    let address='嘉兴市'

    // 方法
    function changeName(){
        name.value='xiaoxiao520'  //修改name 页面无变化
        console.log(name) 
    }
    function changeAge() {
        age.value+=1
    }
    function showTel() {
        alert(tel)
    }
</script>

<style scoped>
    /* 样式 */
    .person{
        background-color: skyblue;
        box-shadow: 0 0 10px;
        border-radius: 10px;
        padding: 20px;
    }
    button{
        margin: 0 5px;
    }
</style>
