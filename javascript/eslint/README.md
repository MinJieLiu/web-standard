# ESLint 配置及规则说明

### 一、包含：

**eslintrc.json**： 该文件可以是你项目中有且仅有ESLint的配置文件，包含简要的规则解释。

### 二、配置文件使用说明

#### 1. 安装依赖：

在`package.json`文件中添加如下依赖（如果没有`package.son`文件需首先通过`npm init` 创建`package.son ` 文件）：

``` json
"devDependencies": {
    "babel-core": "^6.5.2",
    "babel-eslint": "^4.1.8",
    "eslint": "^2.1.0",
    "eslint-plugin-promise": "^1.0.8",
    "eslint-plugin-standard": "^1.3.2"
  }
```

运行如下命令：

> npm install 

#### 2. 将文件夹中的eslintrc.json文件放置在项目根目录

并将`eslintrc.json`重命名为`.eslintrc`(或者直接使用文件夹中的`.eslintrc`文件)

#### 3. 修改配置文件

根据自己项目需要，在配置文件中`globals`配置项中添加项目所需全局变量：举个栗子：

``` javascript
"globals": {
    "document": true,
    "navigator": true,
    "window": true,
    "angular":true // 添加项目所需没有申明的全局变量
  },
```

#### 4. 让ESLint运行起来

修改`package.json`文件。在`script` 配置项中添加如下代码：举个栗子：

``` javascript
  "scripts": {
    "lint": "eslint app.jsx test" //其中app.jsx test需要替换成你项目需要检测的文件或文件夹
  },
```

命令行运行如下代码：

> npm run lint

好了，现在就可以在终端看检测结果了。
