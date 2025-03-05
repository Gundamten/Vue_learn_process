<template>
    <h3>事件修饰符</h3>
    <a @click.prevent="clickHandle" href="https://baidu.com">百战程序员</a>    <!--阻止的是跳转的动作-->
    <div @click="clickDiv">
        <p @click.stop="clickP">测试冒泡</p>
    </div>
</template>
<script>

export default {
    data(){
        return{

        }
    },
    methods:{
        clickHandle(e){
            // 阻止默认事件
            // e.preventDefault();
            console.log("点击了");
        },
        clickDiv(){
            console.log("DIV");            
        },
        clickP(e){
            // e.stopPropagation();
            console.log("P");            
        }
    }
}

</script>