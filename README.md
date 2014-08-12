# CSS3 时钟

请用chrome浏览器查看

<style rel="stylesheet" type="text/css">
body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,
form,fieldset,input,textarea,p,blockquote,th,td {
    padding: 0;
    margin: 0;
}
table {
    border-collapse: collapse;
    border-spacing: 0;
}
fieldset,img {
    border: 0;
}
address,caption,cite,code,dfn,em,strong,th,var {
    font-weight: normal;
    font-style: normal;
}
ol,ul {
    list-style: none;
}
caption,th {
    text-align: left;
}
h1,h2,h3,h4,h5,h6 {
    font-weight: normal;
    font-size: 100%;
}
q:before,q:after {
    content:'';
}
abbr,acronym { border: 0;
}

.clock {
    width: 400px;
    height: 400px;
    border-radius: 200px;
    border: 1px solid #333;
    position: absolute;
    top: 50%;
    left: 50%;
    margin-left: -200px;
    margin-top: -200px;
    font-size: 24px;
    font-family: Constantia, Georgia;
}

.marker {
    text-indent: -999em;
    width: 8px;
    height: 2px;
    background: #333;
}

.item-12 {
    position: absolute;
    left: 196px;
    top: 10px;
}
.item-12 .marker {
    position: absolute;
    top: -8px;
    left: 6px;
    transform: rotate(90deg);
}

.item-1 {
    position: absolute;
    left: 290px;
    top: 36px;
}
.item-1 .marker {
    position: absolute;
    top: -4px;
    left: 9px;
    transform: rotate(120deg);
}

.item-2 {
    position: absolute;
    left: 350px;
    top: 96px;
}
.item-2 .marker {
    position: absolute;
    top: 8px;
    left: 18px;
    transform: rotate(150deg);
}

.item-3 {
    position: absolute;
    right: 16px;
    top: 183px;
}
.item-3 .marker {
    position: absolute;
    top: 16px;
    left: 20px;
    transform: rotate(180deg);
}

.item-4 {
    position: absolute;
    right: 40px;
    top: 267px;
}
.item-4 .marker {
    position: absolute;
    top: 28px;
    left: 20px;
    transform: rotate(210deg);
}

.item-5 {
    position: absolute;
    right: 102px;
    top: 330px;
}
.item-5 .marker {
    position: absolute;
    top: 38px;
    left: 12px;
    transform: rotate(240deg);
}

.item-6 {
    position: absolute;
    left: 198px;
    bottom: 8px;
}
.item-6 .marker {
    position: absolute;
    top: 32px;
    left: 4px;
    transform: rotate(90deg);
}

.item-7 {
    position: absolute;
    left: 112px;
    bottom: 35px;
}
.item-7 .marker {
    position: absolute;
    top: 36px;
    left: -10px;
    transform: rotate(120deg);
}

.item-8 {
    position: absolute;
    left: 44px;
    bottom: 95px;
}
.item-8 .marker {
    position: absolute;
    top: 24px;
    left: -16px;
    transform: rotate(150deg);
}

.item-9 {
    position: absolute;
    left: 14px;
    top: 182px;
}
.item-9 .marker {
    position: absolute;
    top: 18px;
    left: -14px;
}

.item-10 {
    position: absolute;
    left: 42px;
    top: 88px;
}
.item-10 .marker {
    position: absolute;
    top: 10px;
    left: -16px;
    transform: rotate(30deg);
}

.item-11 {
    position: absolute;
    left: 110px;
    top: 26px;
}
.item-11 .marker {
    position: absolute;
    top: 0px;
    left: -8px;
    transform: rotate(60deg);
}

.hour-hand {
    width: 200px;
    height: 4px;
    position: absolute;
    left: 106px;
    top: 200px;
    transform: rotate(90deg);
    -webkit-animation-name: hourmove;
    -webkit-animation-duration: 21600s;
    -webkit-animation-timing-function: linear;
    -webkit-animation-iteration-count: infinite;
}

.minute-hand {
    width: 300px;
    height: 1px;
    position: absolute;
    left: 56px;
    top: 200px;
    transform: rotate(90deg);
    -webkit-animation-name: minutemove;
    -webkit-animation-duration: 3600s;
    -webkit-animation-timing-function: linear;
    -webkit-animation-iteration-count: infinite;
}

@-webkit-keyframes minutemove {
    from {
        transform: rotate(90deg);
    }
    to {
        transform: rotate(450deg);
    }
}

@-webkit-keyframes hourmove {
    from {
        transform: rotate(90deg);
    }
    to {
        transform: rotate(450deg);
    }
}

.hand {
    display: block;
    background: #333;
    width: 50%;
    height: 100%;
}
</style>
<div class="clock">
    <ul>
        <li class="item-12"><span>12</span><span class="marker">-</span></li>
        <li class="item-1"><span>1</span><span class="marker">-</span></li>
        <li class="item-2"><span>2</span><span class="marker">-</span></li>
        <li class="item-3"><span>3</span><span class="marker">-</span></li>
        <li class="item-4"><span>4</span><span class="marker">-</span></li>
        <li class="item-5"><span>5</span><span class="marker">-</span></li>
        <li class="item-6"><span>6</span><span class="marker">-</span></li>
        <li class="item-7"><span>7</span><span class="marker">-</span></li>
        <li class="item-8"><span>8</span><span class="marker">-</span></li>
        <li class="item-9"><span>9</span><span class="marker">-</span></li>
        <li class="item-10"><span>10</span><span class="marker">-</span></li>
        <li class="item-11"><span>11</span><span class="marker">-</span></li>
    </ul>
    <div class="hour-hand">
        <span class="hand"></span>
    </div>
    <div class="minute-hand">
        <span class="hand"></span>
    </div>
</div>
