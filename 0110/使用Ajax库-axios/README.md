### 使用Ajax库-axios

### 1.加入到vue工程

`cd myweb`
`npm install --save --save-exact axios vue-axios`

```
//注册组件
//nano main.js

import axios from 'axios'
import VueAxios from 'vue-axios'
Vue.use(VueAxios, axios)    //注意:VueAxios,后边有个空格，若没有会报错

```

### 2.修改组件

nano HelloWorld.vue

```
<pre>{{contents}}</pre>


export default {
  name: 'HelloWorld',
  data () {
    return {
      contents:""
    }
  },
  mounted(){
	this.axios.post("http://api.komavideo.com/news/list").then(body=>{
		this.contents = body.data;
	});
  }
}
```

### 3.如果有warning报错 问题处理

##### ESLint：Strings must use single quote

##### 解决
```
1、在 .eslintrc.js 配置你的规则rule
rules: {
  ···
  "quotes": [1, "single"], //引号类型 `` "" ''
  ···
}
```

##### 直接修改时.vue文件后，保存编译就报一大堆的错，如何解决？


##### 原因：
因为安装的时候设置了eslint，如果不想有规范的js代码，可以重新初始化关掉eslint。
Use ESLint to lint your code? (Y/n) 这一步选no

如果有良好的规范，其实错误已经很清晰，大多数就是缩进不规范，分号不需要等原因，很容易解决的。写多了就成习惯了。

##### 解决:

在bulid/webpack.base.conf.js里面有配置如下：

```
module: {
	rules: [

...(config.dev.useEslint ? [createLintingRule()] : []),

点进config.dev.useEslint，发现在config/index.js里配置

useEslint: true, // 改为false即可。

```












