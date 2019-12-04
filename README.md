## 项目简述
> 服务器使用express框架搭建，使用http服务，主要用来为onlineExercises项目前端提供题目数据

## 关于服务类型的说明
**miniProgram分支如果需要使用该接口，需要改一下项目中的接口地址**，因为miniProgram分支是微信小程序，需要使用**https服务**，由于证书不便上传，这里只提供了http服务，项目运行过程中如果出现请求错误问题，请大家自行修改一下项目里面的接口地址，这里列出各分支项目中接口位置：
1. miniProgram：app.js
2. questionWithVue：src/api/api.js
3. questionWithServer：js/main.js

运行服务，后台将遍历questions目录下存放的所有excel文件，并读取题库，将读取到的数据规范化为前端需要的数据结构，等待客户端的请求。
题库文件只能为excel表格文件，且题目必须符合一定的格式（题号，题目，四个选项，正确答案）。


在后端目录下cmd运行以下命令即可运行服务：
##### 安装依赖
```# npm install```
##### 运行服务
```# node index.js```
