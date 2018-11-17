# npm-script打造前端工作流

## 技术栈
1. React
2. Redux
3. Ant Design
4. ES6
5. Eslint
6. webpack
7. jest
8. axios

## 目录结构
```
|- build (打包配置目录)
    |- webpack.config.js -- webpack打包基础配置文件
    |- webpack.dev.js -- webpack dev环境打包配置文件
    |- webpack.prod.js -- webpack 生产环境 build打包配置文件
|- dist --目录(构建后目录，用于上线)
|- sh --shell命令文件，用于将develop分支构建在jenkins服务器上执行的脚本
|- node_moudles -- 安装的node包 可以忽略	
|- src (源代码目录)
    |- actions --定义actionTypes和actionCreator
        |- xx(业务目录)
            xx.js 
        |- xx.js --公共的actions
    |- assets  --静态资源目录
        |- fonts --通用字体文件
        |- img 
    |- components --公共组件
        |- BreadCrumb --根据路由匹配的面包屑，名称和层级根据router显示
        |- WeBreadcrumb --可自定义层级和名称的面包屑
			
	|- containers --容器组件目录(展示组件容器，可以用于redux于组件的绑定)
	|- layouts --基础布局组件
    |- middlewares
    |- network 处理网络请求，封装请求函数(axios)
	|- page --目录(页面目录)
		|- xx -- 菜单按照路由的层级规范展示
            |- xx.jsx --匹配路由的容器组件
            |- xx
                |- index.jsx
                |- index.less
                |- mapping.js
    |- reducers
    |- store
    |- utils
        |- index.js --公共函数
        |- config.js --公共的配置项
        |- menu.js --匹配菜单项和路由
        |- reducerUtil.js --优化reducer中switch case的写法
        |- router.js --路由js文件
        |- validate.js --表单项验证的正则
    |- globalConfig.js --全局的请求配置
    |- index.html
    |- index.jsx --入口文件
    |- index.less --全局公共样式
|- tests --jest单元测试目录
|- .babelrc -- babel配置预设和插件，转义新语法，兼容浏览器
|- .eslintignore/.eslintrc.js -- eslint配置
|- .gitlab-ci.yml --git的ci配置，定义不同阶段的不同的job，以及对应的执行命令
|- devServer.js --express 服务文件
|- entrypoint.sh --入口的med-sdk命令
|- nginx.conf --nginx配置
|- package.json -- 纪录基本信息 包括模块依赖关系
|- postcss.config.js --postcss配置，为不同浏览器加前缀
|- README.md -- 项目基本介绍
|- yarn.lock --yarn包文件
```


