<template>
    <div style="height: 30px;line-height: 30px; 
    color: white;padding: 8px;
    background-color: #409EFF;">
        
        <el-row>
            <el-col :span="20">
                币种类型
            </el-col>
            <el-col :span="4"> 
                <i style="font-size: 25px;" class="el-icon-circle-plus"></i>
            </el-col>
        </el-row>
    </div>
     <div>
        <ul>
            <li v-for="item in datas" :key="item">
                {{item.title}}
            </li>       
        </ul>
     </div>   
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Left',
  setup() {
    const datas = [
        {
            title: 'BTC', 
        },
        {
            title: 'ETH', 
        },
        {
            title: 'TRX', 
        }, 
        ];
        return{
            datas
        }
  }
});
</script>