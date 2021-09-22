# week5

## 课程安排
* ajax      
* nodejs    后端
* mysql     数据库

## day5-3

### 知识点
* markdown  一个比html还简单的标识语言

* 静态页面
    * 页面写死，内容固定，维护不方便

* 前端与后端
    * 前端：html+css+js
        * 页面
        ```html
            <!-- index.html -->
            <ul id="list">
                <li>data1</li>
                <li>data2</li>
                <li>data3</li>
                <li>data4</li>
            </ul>
        ```
        ```js
            let data = [
                'data1',
                'data2',
                'data3',
                'data4',
            ]
            const list = document.getElementById('list')

            // ['data1','data2'] -> ['<li>data1</li>','<li>data2</li>']
            const arr = data.map(item=>{
                return `<li>${item}</li>`
            })
            
            // ['<li>data1</li>','<li>data2</li>'] -> '<li>data1</li><li>data2</li>'
            const html = arr.join('')


            list.innerHTML = html;

            <ul id="list">

            </ul>
        ```

    * 后端（服务器）
        > 存放数据的地方

* ajax
    > 利用ajax技术向服务器请求数据到前端
    * 了解前端后端分离
    * 学会查看接口文档
    * 发起ajax请求的步骤
         1. 创建一个异步请求对象
        2. 设置请求参数，建立与服务器连接
        3. 向服务器发送请求
        4. 处理服务器响应数据
        
    * 处理数据，并生产html结构

* 创建本地服务器
    > http-server实现本地服务器
    ```bash
        # 安装
        npm install -g http-server
    ```

### 练习
* 请求接口数据，并渲染到页面