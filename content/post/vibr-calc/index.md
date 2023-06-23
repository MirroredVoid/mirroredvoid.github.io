---
title: 颤音频率计算器
description: 
slug: vibr-calc
date: 2023-06-20T23:30:40Z
image: 
categories:
    - 虚拟歌姬
tags:
    - 在线工具
---
颤音频率计算器，测试博客页面里插入一整个html文件的可行度

<script>
        function Calc(bpm,n){
            var r = Array(2)
            r[1] = 60000/(bpm*n)
            r[0] = 1000/r[1]
            return r
        }

        function Main(){
            var bpm = document.getElementById('bpm').value;
            var n = document.getElementById('n').value;
            var c = Calc(bpm,n)
            document.getElementById('f1').innerText = c[0].toFixed(3)
            document.getElementById('t1').innerText = c[1].toFixed(3)

            c = Calc(bpm,2)
            document.getElementById('f2').innerText = c[0].toFixed(3)
            document.getElementById('t2').innerText = c[1].toFixed(3)
            c = Calc(bpm,3)
            document.getElementById('f3').innerText = c[0].toFixed(3)
            document.getElementById('t3').innerText = c[1].toFixed(3)
            c = Calc(bpm,4)
            document.getElementById('f4').innerText = c[0].toFixed(3)
            document.getElementById('t4').innerText = c[1].toFixed(3)

        }
</script>
<style scoped>
        .link{
            text-decoration: none;
        }

        div.line{
            background:rgba(167, 167, 167, 0.5);
            width: 100%;
            margin-top:12px;
            margin-bottom:12px;
            height:2px;
        }

        div.part{
            display: inline-block;
            margin: 8px;
            margin-top: 2px;
            margin-bottom: 2px;
        }

        div.block{
            background:rgba(232, 232, 232, 0.5);
            border-radius: 16px;
            padding: 16px;
            margin: 16px;
        }

        div.c{
            margin-top: 3px;
            margin-bottom: 3px;
            padding: 3px;
            padding-left: 16px;
            padding-right: 16px;
            border-radius: 12px;
            background-color: #FFF;
            font-size: 100%;
        }
        span.d{
            border-radius: 24px;
            background-color: aqua;
            color: cornflowerblue;
            font-weight: bold;
            float: right;
            padding-left: 12px;
            padding-right: 12px;
        }
        span.r{
            font-family:monospace;
            margin-right: 16px;
            float: right;
        }
        button{
            width: 100%;
            height: 108px;
            margin-top: 6px;
            margin-bottom: 6px;
            border: transparent;
            border-radius: 12px;
            font-size: 240%;
            padding: 6px;
            background-color:deepskyblue;
            color:#FFF;
            -webkit-transition: 0.2s;
            transition: 0.2s;
        }
        button:active{
            background-color:cornflowerblue;
        }

        input{
            width: 100%;
            font-size: 120%;
            margin-top: 6px;
            margin-bottom: 6px;
            padding: 6px;
            padding-left: 16px;
            padding-right: 16px;
            border: transparent;
            border-radius: 12px;
            float: right;
            -webkit-transition: 0.2s;
            transition: 0.2s;
            outline: none;
        }
        input:focus {
            background-color: aqua;
        }

        label{
            font-size: 120%;
            height: 32px;
            margin-top: 6px;
            margin-bottom: 6px;
            padding: 6px;
            float: left;
        }
</style>
<div style="font-size:120%;">
    <div id="title" class="block">
        <div style="font-size: 160%;">颤音频率周期计算器</div>
        <div class="line"></div>
        <div style="color: rgb(167, 167, 167);">“ 波数 ” 指每 1/4 音符长度中包含的颤音周期数量。</div>
    </div>
    <div id="form" class="block" style="padding-bottom:12px;">
        <div class="part" style="width: 100px;">
            <label for="bpm">BPM</label>
            <label for="n">波数</label>
        </div>
        <div class="part" style="width: 32%; float: right; padding-left: 2%;">
            <button id="Main" onclick="Main()" type='button'>计  算</button>
        </div>
        <div class="part" style="width: 48%; float: right;">
            <input id="bpm" type="number" placeholder="BPM" value = "120" min="10" max="999" step="0.001">
            <input id="n" type="number" placeholder="波数" value = "2" min="0.001" max="99" step="0.001">
        </div>

</div>
<div id="out1" class="block">
        <div style="font-size: 120%;">计算结果</div>
        <div class="line"></div>
        <div class="part" style="width: 48%;">
            <div class="c">
                频率
                <span class="d">Hz</span>
                <span class="r" id="f1">---</span>
            </div>
        </div>
        <div class="part" style="width:48%; float: right;">
            <div class="c">
                周期
                <span class="d">ms</span>
                <span class="r" id="t1">---</span>
            </div>
        </div>
    </div>
    <div id="out2" class="block" style="padding-bottom:12px;">
        <div style="font-size: 120%;">常用结果</div>
        <div class="line"></div>
        <div class="part" style="width: 140px;">
            <label>波数 = 2</label>
            <label>波数 = 3</label>
            <label>波数 = 4</label>
        </div>
        <div class="part" style="width:25%; float: right; padding-left: 2%;">
            <div class="c">
                周期
                <span class="d">ms</span>
                <span class="r" id="t2">---</span>
            </div>
            <div class="c">
                周期
                <span class="d">ms</span>
                <span class="r" id="t3">---</span>
            </div>
            <div class="c">
                周期
                <span class="d">ms</span>
                <span class="r" id="t4">---</span>
            </div>
        </div>
        <div class="part" style="width: 25%; float: right;">
            <div class="c">
                频率
                <span class="d">Hz</span>
                <span class="r" id="f2">---</span>
            </div>
            <div class="c">
                频率
                <span class="d">Hz</span>
                <span class="r" id="f3">---</span>
            </div>
            <div class="c">
                频率
                <span class="d">Hz</span>
                <span class="r" id="f4">---</span>
            </div>
        </div>
</div>
<a href="https://space.bilibili.com/510484022" class="link">
        <div class="block" style="color: rgb(167, 167, 167);">
            Bilibili @MirroredVoid
        </div>
</a>

</div>
<!-- </html> -->
