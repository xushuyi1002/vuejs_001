<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        {{ '你好么 Hello World!'}}
        {{ 20 + 1}}
        {{ 'ok'?'yes':'no'}}
        {{ 'hello'.split('').reverse().join('')}}
        <p>
            <span v-once>这个将不会改变: {{ msg }}</span>
        </p>
        <div v-html="rawHtml"></div>
        <!--<a href="http://baidu.com">{{urlName}}</a>-->
        <a v-bind:href="url">{{urlName}}</a>&nbsp;&nbsp;
        <a :href="url">{{urlName1}}</a>
        <div>
            <button v-bind:disabled="isDisabled">Button</button>
        </div>
        <div v-bind:id="dynamicId">动态的Id绑定.</div>
        <div v-bind:id="'list-' + id">hh</div>
        <a v-on:click="doSomething">跳转百度...</a> &nbsp;&nbsp;
        <a @click="doSomething">跳转百度(v-on:click简写)...</a>

        <p v-if="seen">现在你看到我了</p>
        <p v-if="ifSwk">孙悟空</p>
        <p v-else>通臂猿猴</p>

        <!-- v-else 元素必须紧跟在带 v-if 或者 v-else-if 的元素的后面，否则它将不会被识别。 -->
        <div v-if="randomVal>0.5">{{randomVal}} &gt; 0.5. Now you can see me.</div>
        <div v-else>{{randomVal}} &lt; 0.5 .Now you don't see me.</div>

        <p v-show="ifShow">英雄争霸</p>

        <!-- 列表渲染-->
        <ul>
            <li v-for="item in itmes" v-bind:key="item.id">
                {{item}}
            </li>
        </ul>

        <ul>
            <li v-for="(message, index) in messages" v-bind:key="index">
                序号：{{index}} - 姓名：{{message.name}} - 年龄：{{message.age}}
            </li>
        </ul>

        <ul>
            <li v-for="(value, key,index) in obj" v-bind:key="index">
                序号：{{index}} - Key值：{{key}} - Val值：{{value}}
            </li>
        </ul>

    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
        // props: {
        //     msg: String
        // },
        data() {
            return {
                msg: "hello Vuejs.",
                rawHtml: "<span style='color:red'>This should be red.</span>",
                urlName: "淘宝",
                url: "http://taobao.com",
                isDisabled: false,
                dynamicId: 12,
                id: 123,
                urlName1: "淘宝 - v-bind简写",
                seen: true,
                doSomething() {
                    window.location.href = "http://baidu.com";
                },
                ifSwk: true,
                randomVal: Math.random(),
                ifShow: true,
                itmes: ['java', 'js', 'mysql'],
                messages: [
                    {name: 'a', age: 20},
                    {name: 'b', age: 21},
                    {name: 'c', age: 22}
                ],
                obj: {
                    name: "xushuyi",
                    age: 20
                }
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    ul {
        margin: 0;
        padding: 0
    }

    li {
        margin-left: 650px;
        text-align: left;
    }

</style>
