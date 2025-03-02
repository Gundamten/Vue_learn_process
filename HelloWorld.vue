<template>
  <div v-bind:id="title1" v-bind:class="title2">
    <p>剑来</p>
  </div>
  <div v-bind:id="paragraph1" v-bind:class="paragraph2">
  <p>《剑来》是连载于纵横中文网中一部网络玄幻小说，作者是烽火戏诸侯。</p>
  <p>该作品获得第四届橙瓜网络文学奖十大作品、百强作品、 最具潜力十大动漫IP。</p>
  <p>2020年10月《剑来》获第二届泛华文网络文学“金键盘”奖—最佳故事创意奖。</p>
  <p>大千世界，无奇不有。天道崩塌，我陈平安，唯有一剑，可搬山，断江，倒海，降妖，镇魔，敕神，摘星，摧城，开天。</p>
  </div>
  <button v-bind:disabled="dynamicButton" v-bind:class="dynamicButton1">一键三连</button>
</template>
<script>
export default{
  data(){
    return{
      title1:"jianlai1",
      title2:"jianlai2",
      paragraph1:"zhengwen1",
      paragraph2:"zhengwen2",
      dynamicButton:false,
      dynamicButton1:"Button1"
    }
  }
}
</script>

<style>
#jianlai1{
  color:red;
  font-size:30px;
  font-family:"黑体";
  font-weight:bold;
  text-align:center;
  line-height:25px;
}

.zhengwen2{
  color:black;
  font-size:20px;
  font-family:"宋体";
  font-weight:bold;
  text-align:center;
  line-height:20px;
}

.Button1{
  background-color: antiquewhite;
  font-size: 20px;
  position:fixed;
  top:20px;
  right:20px;
}

.Button1:hover {
  background-color:red;
}

.button:active {
  background-color:white;
}
</style>