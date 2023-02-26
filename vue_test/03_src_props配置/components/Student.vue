<template>
  <div>
    <h1>{{ msg }}</h1>
    <h2>学生姓名：{{ name }}</h2>
    <h2>学校性别：{{ sex }}</h2>
    <h2>学校年龄：{{ myAge+1 }}</h2>
    <button @click="updateAge">尝试修改收到的年龄</button>
  </div>
</template>

<script>
export default {
  name: "Student",
  data() {
    return {
      msg:'欢迎学习Vue',
      myAge:this.age
     
    };
  },
  methods: {
    updateAge(){
      this.myAge++
    }
  },
  // 简单声明接收
  // props:['name','age','sex']

  // 接收的同时对数据进行类型限制
  /* props:{
    name:String,
    age:Number,
    sex:String
  } */

  props:{
    name:{
      type:String, //name的类型是字符串
      required:true,//name是必要的的
    },
    age:{
      type:Number,
      default:99//默认值
    },
    sex:{
      type:String,
      required:true
    }
  }
};
</script>

<style>
.school {
  background-color: gray;
}
</style>