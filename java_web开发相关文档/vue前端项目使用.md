# Vue创建项目

在目录下

1. 创建项目

```
vue create vue-project01
```

2. 视图

```vue ui
vue ui
```



# element-ul下载与使用

1. 下载

```
npm install element-ui@2.15.3
```

2. 使用:

   在main.js下面导入element组件

   ```
   // 导入element
   import ElementUI from 'element-ui'
   import 'element-ui/lib/theme-chalk/index.css';
   // 使用
   Vue.use(ElementUI);
   ```

# 显示页面

1. 先新建一个.vue组件

![image-20230904212114702](C:/Users/xtk/AppData/Roaming/Typora/typora-user-images/image-20230904212114702.png)

2. 在APP.vue里引用组件名

![image-20230904212125501](C:/Users/xtk/AppData/Roaming/Typora/typora-user-images/image-20230904212125501.png)

3. 还要导入该vue组件

![image-20230904212155719](C:/Users/xtk/AppData/Roaming/Typora/typora-user-images/image-20230904212155719.png)