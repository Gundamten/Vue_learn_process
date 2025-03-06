<!-- 获取DOM的操作 -->
<template>
    <div ref="container" class="container">{{ content }}</div>
    <input type="text" ref="username">
    <button @click="getElementHandle">获取元素</button>
</template>
<script>
// 内容改变：{{模板语法}}
// 属性改变：v-bind:指令
// 事件：v-on:click

// 如果没有特别的需求，不要操作DOM
export default {
    data(){
        return{
            content:"内存"
        }
    },
    methods:{
        getElementHandle(){
            // innerHTML:原生JS的属性
            console.log(this.$refs.container.innerHTML = "哈哈哈");    //获取并修改div中的内容
            console.log(this.$refs.username.value);    //获取input中的内容
        }
    }
}

</script>