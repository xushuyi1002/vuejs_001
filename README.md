# vuejs_001

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### Xusy At 20190105 Start Studing Vuejs...
1. 安装Vue
```
注：node版本必须大于或等于8.9版本
   vue-cli3.x: npm install -g @vue/cli
   vue-cli2.x: npm install -g @vue/cli-init
```
2. 创建项目 
```
vue init webpack my-project
注：安装依赖的时候 选择最后一个，就是自己安装
cd my-project
npm start/npm run dev
```
3. 工程目录

4. 基础指令
```
https://cn.vuejs.org/v2/guide/syntax.html
1. Mustache：{{ 变量 }} 只能存在单行语句
2. v-once：只能够渲染一次
3. v-html：解析html结构
4. v-bind：指令（解析属性中的对象）
5. v-bind简写：（:）
6. v-if：条件渲染
7. v-show：条件渲染
```
5. v-if vs v-show
```
v-if 是“真正”的条件渲染，因为它会确保在切换过程中条件块内的事件监听器和子组件适当地被销毁和重建。
v-if 也是惰性的：如果在初始渲染时条件为假，则什么也不做——直到条件第一次变为真时，才会开始渲染条件块。
相比之下，v-show 就简单得多——不管初始条件是什么，元素总是会被渲染，并且只是简单地基于 CSS 进行切换。
一般来说，v-if 有更高的切换开销，而 v-show 有更高的初始渲染开销。因此，如果需要非常频繁地切换，则使用 v-show 较好；如果在运行时条件很少改变，则使用 v-if 较好。
```
6. html 代码实现一些符号，大于号、小于号、商标等
```
 &lt;  	 < 	 小於号或显示标记    
 &gt;	     >	     大於号或显示标记
 &amp;     &	     可用於显示其它特殊字符  
 &quot;	 "	     引号
 &reg;	     ®	     己注册
 &copy; 	 ©	     版权
 &trade;	 ™	     商标
 &ensp;	 	     半方大的空白
 &emsp;	 	     全方大的空白
 &nbsp;	 	     不断行的空白
```


