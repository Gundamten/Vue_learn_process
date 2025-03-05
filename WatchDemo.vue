<template>
    <h3>侦听器</h3>
    <p>{{ message }}</p>
    <button @click="updateHandle">修改数据</button>
</template>
<script>

export default {
    data(){
        return{
            message:"Hello"
        }
    },
    
    methods:{
        updateHandle(){
            this.message="World"
        }
    },

    // 侦听器
    watch:{
        // newValue: 改变之后的数据
        // oldValue: 改变之前的数据
        // 函数名必须与侦听的数据对象保持一致
        message(newValue,oldValue){    //要与data中定义的对象名字保持一致
            // 数据发生变化，自动执行的函数
            console.log(newValue,oldValue);
            
        }
    }
}

</script>