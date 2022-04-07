index.html 裡面寫

<body>
    <div id="app">
        <h2>My name is {{ name }}</h2>
        <input type="text" v-model="name">
    </div>

    <script>
        let app = new Vue({
            el: '#app',
            data: {
                name: 'teddy',
            },
        });
    </script>
</body>

重點一
執行步驟1. <input type="text" v-model="name"> 打字
執行步驟2. data name 會被修改
執行步驟3. h2也會一起修改

