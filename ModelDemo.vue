<template>
    <h3>表单输入绑定</h3>
    <form>
        <input type="text" v-model.lazy="message">
        <p>{{ message }}</p>
        <!-- 复选框 -->
        <input type="checkbox" id="checkbox" v-model="checked" />
        <label for="checkbox">{{ checked }}</label>
    </form>
</template>
<script>

export default {
    data(){
        return{
            message:'',
            checked:false
        }
    }
}

</script>