index.html 裡面寫

<body>
    <div id="app">
        <p v-if="name">Vue JS</p>
        <p v-if="age">24</p>

        <button @click="ShowName"> 姓名顯示 | 姓名隱藏 </button>
        <button @click="ShowAge"> 年齡顯示 | 年齡隱藏</button>
    </div>

    <script>
        let app = new Vue({
            el: '#app',
            data: {
                name: true,
                age: true,
            },
            methods: {
                ShowName() {
                    this.name = !this.name
                },
                ShowAge() {
                    this.age = !this.age
                }
            }
        });
    </script>
</body>



重點一
v-if 存在 true 和 false 
true 為是 為顯示
false 為否 為不顯示

ShowName() {
    this.name = !this.name
},
ShowAge() {
    this.age = !this.age
}

this.name 原本是 是(顯示) 但是按下函式後 否定了是(顯示) 所以變成否(不顯示)
this.age 原本是 是(顯示) 但是按下函式後 否定了是(顯示) 所以變成否(不顯示)

