<template>
    <h3>{{ itbaizhan.name }}</h3>
    <!-- <p>{{ itbaizhan.content.length > 0 ? 'Yes' : 'No' }}</p>    官方不推荐将运算放在这里 -->
     <p>{{ itbaizhanContent }}</p>    <!--计算属性不需要加括号-->
     <p>{{ itbaizhanContents() }}</p>     <!--函数需要加括号-->
</template>
<script>

export default {
    data(){
        return{
            itbaizhan:{
                name:"百战程序员",
                content:["前端","Java","python"]
            }
        }
    },
    // 计算属性
    computed:{
        itbaizhanContent(){
            return this.itbaizhan.content.length > 0 ? 'Yes' : 'No'
        }
    },
    // 或者将其放在methods方法当中
    methods:{
        itbaizhanContents(){
            return this.itbaizhan.content.length > 0 ? 'Yes' : 'No'
        }      
    }
}

</script>