index.html 裡面寫

<body>
    <div id="app">
        <div v-if="type === 'A'">
            A
        </div>
        <div v-else-if="type === 'B'">
            B
        </div>
        <div v-else-if="type === 'C'">
            C
        </div>
        <div v-else>
            Not A/B/C
        </div>
    </div>

    <script>
        let app = new Vue({
            el: '#app',
            data: {
                type: 'A'
            },
            methods: {

            }
        });
    </script>
</body>

重點一
v-else-if 需要與 v-if 一起使用

data: {
    type: 'A'
},

type 輸入A顯示A
type 輸入B顯示B
type 輸入C顯示C
type 輸入其他顯示  Not A/B/C


