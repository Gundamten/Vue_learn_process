<template>
    <h3>Key属性添加到v-for中</h3>
    <p v-for="(item,index) in names" :key="index">{{ item }}</p>
    <div v-for="item in result" :key="item.id">
        <p>{{ item.title }}</p>
        <img v-bind:src="item.avator" alt="">
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
        }
    }
}

</script>