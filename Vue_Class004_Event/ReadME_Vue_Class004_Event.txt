index.html 裡面寫

<body>
    <div id="app">
        <p>我每個月賺{{dollar}}</p>

        <div>
            <button v-on:click="dollar++"> +1 </button>
            <button v-on:click="dollar--"> -1 </button>
        </div>

        <div>
            <button @dblclick="Amount(5)"> +5 </button>
            <button @click="Amount(-5)"> -5 </button>
        </div>
    </div>

    <script>
        let app = new Vue({
            el: '#app',
            data: {
                dollar: 100,
            },
            methods: {
                Amount(pound) {
                    this.dollar += pound
                }
            }
        });
    </script>
</body>


重點一  第一種寫法
原本寫法  <button click="dollar++"> +1 </button>
Vue寫法  <button v-on:click="dollar++"> +1 </button>


重點二  第二種寫法
原本寫法  <button click="Amount(-5)"> -5 </button>
Vue寫法  <button @click="Amount(-5)"> -5 </button>

ps.都是在 data 裡面定義好再回傳出去

補充一
Amount(pound) {
    this.dollar += pound
}

pound = 5
dollar = 100

this.dollar += pound // 105 = 100 + (5)

pound = -5
dollar = 100

this.dollar += pound // 95 = 100 + (-5)

補充二
@dblclick //在很短的時間內發生兩次 click，即是一次 double click 事件。