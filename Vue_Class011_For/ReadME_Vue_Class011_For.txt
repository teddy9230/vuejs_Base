index.html 裡面寫

<body>
    <div id="app">
        <ol>
            <li v-for="text in texts">{{ text }}</li>
        </ol>

        <ul>
            <li v-for="fruit in fruits">{{ fruit.name }}|{{ fruit.color }}|{{ fruit.weight }} </li>
        </ul>
    </div>

    <script>
        let app = new Vue({
            el: '#app',
            data: {
                texts: ['A', 'B', 'C', 'D', 'E'],
                fruits: [
                    { name: 'Mango', color: 'Orange', weight: 200 },
                    { name: 'Apple', color: 'Red', weight: 200 },
                    { name: 'Banana', color: 'Yello', weight: 200 }
                ],
            },
            methods: {

            }
        });
    </script>
</body>

重點一
以往正常寫法 @foreach($product as $row)
Vue寫法  <li v-for="text in texts">{{ text }}</li>
Vue寫法  <li v-for="fruit in fruits">{{ fruit.name }}|{{ fruit.color }}|{{ fruit.weight }} </li>
