index.html 裡面寫

<head>
    <style>
        .canvas {
            height: 300px;
            width: 300px;
            margin-top: 20px;
            background-color: orange;
        }
    </style>
</head>

<body>
    <div id="app">
        <button @click="eventObject"> eventObject </button>

        <div class="canvas" @mousemove="over">
            {{ mousemoveXY.x }}, {{ mousemoveXY.y }}
        </div>
    </div>

    <script>
        let app = new Vue({
            el: '#app',
            data: {
                mousemoveXY: {
                    x: 0,
                    y: 0
                }
            },
            methods: {
                eventObject(event) {
                    console.log(event);
                },
                over(e) {
                    this.mousemoveXY.x = event.offsetX,
                        this.mousemoveXY.y = event.offsetY
                },
            }
        });
    </script>
</body>


重點一
<button @click="eventObject"> eventObject </button>

methods: {
    eventObject(event) {
        console.log(event);
    },
}

event 裡面記錄很多資訊 包含使用滑鼠點擊等等

重點二  第二種寫法
<div class="canvas" @mousemove="over">
    {{ mousemoveXY.x }}, {{ mousemoveXY.y }}
</div>

data: {
    mousemoveXY: {
        x: 0,
        y: 0
    }
},
methods: {
    over(e) {
        this.mousemoveXY.x = event.offsetX,
        this.mousemoveXY.y = event.offsetY
    },
}

步驟1. class="canvas" 定義好一個 300 * 300 的橘色方塊
步驟2. data mousemoveXY 定義一個 X座標=0 Y座標=0 的起始值
步驟3. 設定 @mousemove="over" 滑鼠移動
步驟4. methods over 滑鼠碰到後找到當前的 X座標 以及 Y座標


ps.都是在 data 裡面定義好再回傳出去

補充一
over(e) {
    this.mousemoveXY.x = event.offsetX,
    this.mousemoveXY.y = event.offsetY
},

offsetX offsetY 是event裡面其中兩個屬性(還有很多其他的屬性)