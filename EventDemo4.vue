<template>
    <h3>内联事件处理器</h3>
    <button @click="addCount('hello')">Add</button>    <!--@符号是由v-on:简化而成的-->
    <p>{{ count }}</p>
</template>
<script>

export default{
    data(){
        return{
            count:0
        }
    },
    // 所有的方法或者函数都放在这里
    methods:{
        // event对象
        addCount(msg){
            // 读取到data里面的数据的方案：this.count
            // Vue中的event对象，就是原生JS的Event对象
            // e.target.innerHTML = "Add" + this.count;
            console.log(msg);
            this.count++
        }
    }
}

</script>