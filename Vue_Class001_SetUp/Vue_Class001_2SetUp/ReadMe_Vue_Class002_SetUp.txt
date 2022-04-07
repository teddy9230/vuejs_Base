<body>
    <div id="app">
        <h1> {{ name }} </h1>
    </div>

    <script>
        let app = new Vue({
            el: '#app',
            data: {
                name: 'learn Vue',
            }
        });
    </script>
</body>

以上為分開一支檔案

id="app" 必須要與 el:'#app' app需要一致
如果要更改為 id="test" 必須要與 el:'#test' test需要一致


重點一
<script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script> 要先引入

id="app" 必須要與 el:'#app' app需要一致
如果要更改為 id="test" 必須要與 el:'#test' test需要一致

重點二
<h1> {{ name }} </h1> 必須要與 name:'learn Vue' name需要一致
如果要更改為 <h1> {{ message }} </h1> 必須要與 message:'learn Vue' message需要一致