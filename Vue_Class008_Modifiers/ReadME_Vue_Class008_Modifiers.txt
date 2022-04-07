index.html 裡面寫

<body>
    <div id="app">
        <h1>{{ name }}</h1>
        <button @click="Message">變更</button>
        <button @click.alt="Message">按住alt才會變更</button>
        <button @click.shift="Message">按住shift才會變更</button>
    </div>

    <script>
        let app = new Vue({
            el: '#app',
            data: {
                name: 'teddy',
            },
            methods: {
                Message() {
                    console.log('change teddy')
                }
            }
        });
    </script>
</body>


重點一
@click.alt 按住alt才會變更
@click.shift 按住shift才會變更