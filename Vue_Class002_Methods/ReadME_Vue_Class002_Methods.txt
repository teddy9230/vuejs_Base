index.html 裡面寫

<body>
    <div id="app">
        <h1> {{ MyName()}} </h1>
        <h1> {{ MyAge(24)}} </h1>
    </div>

    <script>
        let app = new Vue({
            el: '#app',
            data: {
                message: 'teddy',
            },
            methods: {
                MyName() {
                    return 'teddyLin'
                },
                MyAge(age) {
                    return `${this.message} My age is ${age}`
                },
            },
        });
    </script>
</body>

重點一 
methods: {
    MyName() {
        return 'teddyLin'
    },
    MyAge(age) {
        return `${this.message} My age is ${age}`
    },
},
丟進去是一個函式


重點二
MyAge(age) {
    return `${this.message} My age is ${age}`
},

 return `${this.message} My age is ${age}` 
 `${ }`  ES6 模板字符串