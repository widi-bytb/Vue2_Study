<template>
   <div class="app">
    <h1>{{msg}},学生姓名是：{{studentName}}</h1>
    <!-- 通过父组件给子组件传递函数类型的props实现：子给父传递数据 -->
    <School :getSchoolName="getSchoolName"/>

    <!-- 通过父组件给子组件绑定自定义事件实现：子给父传递数据（第一种写法，使用@or v-on） -->
    <!-- <Student @getName="getStudentName"/> -->
    
    <!-- 通过父组件给子组件绑定自定义事件实现：子给父传递数据（第二种写法，使用ref） -->
    <Student ref="student" @click.native="show"/>
   </div>
</template>

<script>
    import Student from './components/Student.vue'
    import School from './components/School.vue'

    export default {
        name:'App',
        components:{Student,School},
        data() {
            return {
                msg:'你好啊！',
                studentName:''
            }
        },
        methods: {
            getSchoolName(name){
                console.log('App组件收到了',name)
            },
            getStudentName(name){
                console.log('App组件收到了',name)
                this.studentName = name
            },
            show(){
                alert(123)
            }
        },
        mounted() {
            this.$refs.student.$on('getName',this.getStudentName) //绑定自定义事件
            // this.$refs.student.$once('getName',this.getStudentName) //绑定自定义事件（一次性）
        },
    }
</script>

<style>
.app{
    background-color: gray;
    padding:5px;
}
</style>