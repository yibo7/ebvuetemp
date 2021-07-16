<template>
    <el-container>
    <!-- 顶栏 -->
    <!-- <el-header height="30">
      <h5>Element 页面布局</h5>
    </el-header> -->
    <!-- 嵌套容器 -->
    <el-container>
      <!-- 侧边导航菜单 -->
      <el-aside  width="200px">
        <Left/>
      </el-aside>
      <!-- 内容 -->
      <el-main>
        <!-- 第一列栅格布局 -->
        <el-row>
          <el-col :span="12" class="col1"></el-col>
          <el-col :span="12" class="col2"></el-col>
        </el-row>
        <!-- 第二列布局 -->
        <el-row>
          <el-col :span="24" class="col3"></el-col>
        </el-row>
      </el-main>
    </el-container>
    <!-- 底栏 -->
    <!-- <el-footer height="30px">&copy; xxx 2019</el-footer> -->
  </el-container> 
</template> 
 
<script lang="ts">
import { defineComponent } from 'vue';
import  Left  from './components/Left.vue';
// import HelloWorld from './components/HelloWorld.vue'; 
export default defineComponent({
  name: 'App',
  components: {
     Left
  },
  // setup(){
  //       // const sonRef = ref(HelloWorld);
  //       // function onPAdd() {
  //       //     sonRef.value?.onAdd();
  //       // }
  //       return {
  //           collapsed: false,
  //       }
  // }
   
});
</script>

<style>
  
html,
body {
            margin: 0;
            padding: 0;
            height: 100%;
        }
 #app,.box{
            height: 100%;
        }
.el-container {
            height: 100%;
        }
.el-header {
  background-color: #409EFF;
  color: white;
  /* height:  30px !important;
  line-height: 30px !important; */
}
.el-footer {
  background-color: #909399;
  color: black;
  text-align: center;
}
.el-aside {
  height: 100%;
  background-color: rgb(248, 248, 248);
}
.el-main {
  background-color: rgb(240, 240, 240);
  
}
.el-col {
  height: 200px;
}
.col1 {
  background-color: teal;
}
.col2 {
  background-color: tomato;
}
.col3 {
  background-color: thistle;
} 
</style>
