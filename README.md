## 功能介绍


- 医生管理：管理系统可以录入、修改和查询医生的基本信息，如名称、价格、职称、在诊时间、简介等。
- 科室管理：系统可以管理医生的科室信息，包括科室的名称等。
- 评论管理：管理和浏览整个网站的评论信息。
- 用户管理：管理和浏览网站的用户信息，可以新增、编辑和删除用户。
- 统计分析：系统可以根据医生的活动数据和用户参与度进行统计和分析，帮助管理员了解整个系统的状况。
- 消息管理：医生管理员可以在系统上发布消息，整个网站的用户都能收到。
- 广告管理：医生管理员可以在系统上发布广告消息，然后在详情页面右侧展示。
- 意见反馈：医生管理员可以在后台查看浏览用户提交的意见反馈信息。
- 系统信息：管理员可以查看系统的基本信息，包括系统名称、服务器信息、内存信息、cpu信息、软件信息等。
- 注册登录：用户通过注册和登录后，才能使用网站。
- 门户浏览：用户进入首页后，可以浏览医生列表信息，包括最新、最热。
- 热门推荐：基于协同过滤推荐算法的热门推荐。
- 用户中心：包括用户基本资料修改、用户基本信息、密码、收藏点赞等。
- 我的预约：包括我预约的医生的挂号信息。
- 意见反馈：包括用户提交意见反馈的入口页面。
- 模糊搜索：顶部搜索功能，支持模糊搜索医生信息。
- 医生评论：详情页下侧用户可以评论医生。

## 开发环境

- 后端： Python 3.8 + Django 3.2
- 前端： Javascript + Vue
- 数据库：MySQL 5.7
- 开发平台：Pycharm + vscode
- 运行环境：Windows 11

### 后端技术

#### django框架

Django是一款基于Python开发的全栈式一体化Web应用框架。2003年问世之初，它只是美国一家报社的内部工具，2005年7月使用BSD许可证完成了开源。Django采用MTV设计模式，即Model（模型）+ Template（模板）+ View（视图）。它遵循MVC设计，并且内置了对象关系映射（ORM）层，使得开发者无需关心底层的数据存取细节，可以更专注于业务逻辑的开发。

Django的目的是削减代码量，简单且迅速地搭建以数据库为主体的复杂Web站点。它是全栈式框架，因此安装起来很简单，而且使用者众多。这使得Django除具有完备的官方文档之外，还有大量的关联文档、丰富的第三方库可供使用。与其他框架相比，Django用起来要轻松得多。

优点：

- 提供了定义序列化器Serializer的方法。可以快速根据Django ORM或者其他库自动序列化或反序列化。
- 提供了丰富的类视图MIXIN扩展类。可以简化视图的编写。
- 具有丰富的定制层级。包括函数视图、类视图，还可以将视图与自动生成API结合，满足各种需求。
- 支持多种身份认证和权限认证方式。
- 内置了限流系统。

### 前端技术

- npm：node.js的包管理工具，用于统一管理我们前端项目中需要用到的包、插件、工具、命令等，便于开发和维护。
- ES6：Javascript的新版本，ECMAScript6的简称。利用ES6我们可以简化我们的JS代码，同时利用其提供的强大功能来快速实现JS逻辑。
- vue-cli：Vue的脚手架工具，用于自动生成Vue项目的目录及文件。
- vue-router： Vue提供的前端路由工具，利用其我们实现页面的路由控制，局部刷新及按需加载，构建单页应用，实现前后端分离。
- vuex：Vue提供的状态管理工具，用于统一管理我们项目中各种数据的交互和重用，存储我们需要用到数据对象。
- Ant-design：基于MVVM框架Vue开源出来的一套前端ui组件。
- Axios是一个基于Promise的HTTP客户端，用于浏览器和node.js。它提供了一个简单的API来发送HTTP请求，支持从浏览器中创建 XMLHttpRequests。Axios常用于与后端API进行通信，处理异步请求和响应。

## 代码结构

### 后端结构

```
server  
├── myapp            // 主应用
│       └── auth                     // 认证管理
│       └── middlewares              // 中间件
│       └── permission               // 权限
│       └── views                    // 视图与接口（主要业务代码）
│       └── models.py                // 状态码
│       └── serializers.py           // 状态码
│       └── urls.py                  // 状态码
│       └── utils.py                 // 状态码
├── server             // 配置目录
├── upload             // 静态资源目录
├── requirements.txt    // 依赖项
```

### 前端结构

```
├── build                      // 构建相关  
├── public                     // 公共文件
│   ├── favicon.ico            // favicon图标
│   └── index.html             // html模板
├── src                        // 源代码
│   ├── api                    // 所有请求
│   ├── assets                 // 主题 字体等静态资源
│   ├── router                 // 路由
│   ├── store                  // 全局 store管理
│   ├── utils                  // 全局公用方法
│   ├── views                  // view界面
│   ├── App.vue                // 入口页面
│   ├── main.js                // 入口 加载组件 初始化等
│   └── settings.js            // 系统配置
├── .eslintignore              // 忽略语法检查
├── .eslintrc.js               // eslint 配置项
├── .gitignore                 // git 忽略项
├── babel.config.js            // babel.config.js
├── package.json               // package.json
└── vite.config.js             // vue配置
```

