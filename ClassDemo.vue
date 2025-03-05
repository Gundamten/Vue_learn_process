<template>
    <p :class="{'active' :isActive,'text-danger':hasError}">Class样式绑定1</p>
    <p :class="classObject">Class样式绑定2</p>
    <p :class="[arrActive,arrHasError]">Class样式绑定3</p>
    <p :class="[isActive ? 'active' : '']">Class样式绑定4</p>    <!--三元表达式-->
    <!-- 温馨提示：数组和对象嵌套过程中，只能是数组嵌套对象，不能反其道而行 -->
     <p :class="[isActive ? 'active' : '',{'text-danger':hasError}]">Class样式绑定5</p>
</template>
<script>

export default {
    data(){
        return{
            isActive:true,
            hasError:false,
            classObject:{
                'active':false,
                'text-danger':true
            },
            arrActive:"active",
            arrHasError:"text-danger"
        }
    }
}

</script>

<style>

/* 控制样式是否展示 */
.active{
    font-size:30px;
}

.text-danger{
    color:red;
}

</style>