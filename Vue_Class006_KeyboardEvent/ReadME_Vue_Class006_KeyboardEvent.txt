index.html 裡面寫

<body>
    <div id="app">
        <h2>My name is {{ name }}</h2>
        <input type="text" @keyup="NameChange">
    </div>

    <script>
        let app = new Vue({
            el: '#app',
            data: {
                name: 'teddy'
            },
            methods: {
                NameChange(e) {
                    // console.log(e.target.value);
                    this.name = e.target.value;
                }
            }
        });
    </script>
</body>

重點一
<input type="text" @keyup="NameChange">
@keyup 紀錄鍵盤按過的按鍵


NameChange(e) {
    // console.log(e.target.value);
    this.name = e.target.value;
}

@keyup 紀錄鍵盤按過的按鍵 e.target.value
e.target.value 替換 name


