<template>
    <h3>列表渲染</h3>
    <p v-for="(item,index) in names">{{ item }}-{{ index }}</p>
    <div v-for="item in result">
        <p>{{ item.title }}</p>
        <img v-bind:src="item.avator" alt="">
    </div>
    <div>
        <p v-for="(value,key,index) in userInfo">{{ value }}-{{ key }}-{{ index }}</p>    <!--这里的of和原来的in可以相互替换-->
    </div>
</template>
<script>

export default {
    data(){
        return{
            names:["百战程序员","尚学堂","IT"],
            result: [
                {
                    "id":2255,
                    "title":"便哈哈读书符合",
                    "avator":"https1",
                },
                {
                    "id":5555,
                    "title":"华赛社费",
                    "avator":"https2",
                },
                {
                    "id":3333,
                    "title":"撒上的活塞机",
                    "avator":"https3",
                },
            ],
            userInfo: {
                name:"iwen",
                age:20,
                sex:"男"
            }
        }
    }
}

</script>