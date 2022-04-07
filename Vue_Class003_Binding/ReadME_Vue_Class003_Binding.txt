index.html 裡面寫

<head>
    <style>
        .red {
            color: red;
        }

        .decoration {
            text-decoration: line-through;
        }
    </style>
</head>

<body>
    <div id="app">
        <a v-bind:href="address"> Vue Js</a>
        <p :class="classes">Vue JS</p>
        <input type="text" v-bind:value="name">
    </div>

    <script>
        let app = new Vue({
            el: '#app',
            data: {
                address: 'https://v2.vuejs.org/v2/guide/',
                classes: ['red', 'decoration'],
                name: 'teddy',
            },
        });
    </script>
</body>

重點一 超連結
原本寫法  <a href="https://v2.vuejs.org/v2/guide/"> Vue Js</a>
Vue寫法  <a v-bind:href="address"> Vue Js</a>


重點二 樣式
原本寫法  <p class="classes">Vue JS</p>
Vue寫法  <p :class="classes">Vue JS</p>

重點三 表格
原本寫法  <input type="text" value="name">
Vue寫法   <input type="text" v-bind:value="name">

ps.都是在 data 裡面定義好再回傳出去