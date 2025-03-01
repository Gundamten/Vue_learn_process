<template>
  <h3>模板语法</h3>
  <p>{{ msg }}</p>
  <p>Hello World</p>
  <p>{{ number + 1 }}</p>
  <p>{{ ok ? 'Yes' : 'No' }}</p>
  <p>{{ message.split('').reverse().join('') }}</p>
  <p>{{ rawHtml }}</p>   <!-- 这一步不能只会显示引号内的所有内容 -->
  <p v-html = "rawHtml"></p>  <!--这样才能识别链接-->
</template>

<script>
export default{
  data(){
    return{
      msg:"神奇的语法",
      number:10,
      ok:true,
      message:"大家好",
      rawHtml:"<a href = 'https://itbaizhan.com'>百战程序员</a>"
    }
  }
}
</script>



