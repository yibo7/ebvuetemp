# vue+electron手脚架
 
 ## 一.安装 ant-design ui框架
 ```
  npm install ant-design-vue --save
 ```

##二.让父组件调用子组件的方法
主要在父组件中设置
模板指定ref
```html
<HelloWorld ref="sonRef" />
```
在setup中这样调用:
``` js

const sonRef = ref(HelloWorld);//HelloWorld为子组件
        function onPAdd() {
            sonRef.value?.onAdd();
        }
```
## 让.vue能提供style自动完成
在当前项目下创建文件夹 .vscode 并在里面创建一个文件 settings.json,添加内容如下:
``` json
{
    "files.associations": {
        "*.vue": "html"
    }
}
```

