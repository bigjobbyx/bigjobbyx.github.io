---
layout: page
title: Juzo
permalink: /juzo/
---
 <html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Color Grid</title>
    <style>

body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    height: 100vh;
    margin: 0;
    background-color: #f0f0f0;
}

        .container {
            width: 100vw;
            display: flex;
            flex-wrap: wrap;
        }

        @media (orientation: portrait) {
            .color-square {
                width: 100vw;
                height: calc(100vw * 0.25);
            }
        }

        @media (orientation: landscape) {
            .container {
                flex-direction: row;
            }
            .color-square {
                width: 33.33vw;
                height: calc(33.33vw * 0.25);
            }
        }

        .color-square {
            position: relative;
        }

        .color-label {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
            font-weight: bold;
            font-size: 16px;
            text-shadow: -1px -1px 0 #000,  
                         1px -1px 0 #000,
                         -1px 1px 0 #000,
                         1px 1px 0 #000;
        }
    </style>
</head>
<body>

<div class="container">
    <div class="color-square" style="background-color: #000000;"><span class="color-label">Black pepper</span></div>
    <div class="color-square" style="background-color: #ffffff;"><span class="color-label">White</span></div>
    <div class="color-square" style="background-color: #DEDEDE;"><span class="color-label">Light Grey</span></div>
    <div class="color-square" style="background-color: #9f8277;"><span class="color-label">Pearl</span></div>
    <div class="color-square" style="background-color: #958072;"><span class="color-label">Coffee creme</span></div>
    <div class="color-square" style="background-color: #ceb5a1;"><span class="color-label">Sandel</span></div>
    <div class="color-square" style="background-color: #664e40;"><span class="color-label">Cacao</span></div>
    <div class="color-square" style="background-color: #cdb09f;"><span class="color-label">Make-Up</span></div>
    <div class="color-square" style="background-color: #D0B4A6;"><span class="color-label">Beige</span></div>
    <div class="color-square" style="background-color: #A59B8F;"><span class="color-label">Sepia</span></div>
    <div class="color-square" style="background-color: #A48F70;"><span class="color-label">Cashmere</span></div>
    <div class="color-square" style="background-color: #d0bca6;"><span class="color-label">Cardamom</span></div>
    <div class="color-square" style="background-color: #b7a090;"><span class="color-label">Silk</span></div>
    <div class="color-square" style="background-color: #C5BEB4;"><span class="color-label">Sand</span></div>
    <div class="color-square" style="background-color: #867c6b;"><span class="color-label">Unique Taupe</span></div>
    <div class="color-square" style="background-color: #776546;"><span class="color-label">Smoke</span></div>
    <div class="color-square" style="background-color: #c2b19e;"><span class="color-label">Almond</span></div>
    <div class="color-square" style="background-color: #d5c8b2;"><span class="color-label">Sesame</span></div>
    <div class="color-square" style="background-color: #d5c8b2;"><span class="color-label">Light beige</span></div>
    <div class="color-square" style="background-color: #9a7d66;"><span class="color-label">Anise</span></div>
    <div class="color-square" style="background-color: #a4917b;"><span class="color-label">Nutmeg</span></div>
    <div class="color-square" style="background-color: #aea40c;"><span class="color-label">Smooth Olive</span></div>
    <div class="color-square" style="background-color: #57A434;"><span class="color-label">Glowing Green</span></div>
    <div class="color-square" style="background-color: #b1ceb3;"><span class="color-label">Stunning Green</span></div>
    <div class="color-square" style="background-color: #257b80;"><span class="color-label">Deep Aqua</span></div>
    <div class="color-square" style="background-color: #0384BB;"><span class="color-label">Ionic Blue</span></div>
    <div class="color-square" style="background-color: #9fc4d6;"><span class="color-label">Mellow Blue</span></div>
    <div class="color-square" style="background-color: #7694b6;"><span class="color-label">Awesome Blue</span></div>
    <div class="color-square" style="background-color: #254377;"><span class="color-label">Blueberry</span></div>
    <div class="color-square" style="background-color: #254290;"><span class="color-label">Dark Blue Sensation</span></div>
    <div class="color-square" style="background-color: #161F62;"><span class="color-label">Dark blue</span></div>
    <div class="color-square" style="background-color: #08112F;"><span class="color-label">Navy</span></div>
    <div class="color-square" style="background-color: #06092A;"><span class="color-label">Marine (FR)</span></div>
    <div class="color-square" style="background-color: #08112F;"><span class="color-label">Marine</span></div>
    <div class="color-square" style="background-color: #2e2c52;"><span class="color-label">Night Blue</span></div>
    <div class="color-square" style="background-color: #06092a;"><span class="color-label">Juniper</span></div>
    <div class="color-square" style="background-color: #2E2635;"><span class="color-label">Romance</span></div>
    <div class="color-square" style="background-color: #3B2762;"><span class="color-label">Purple Lightning</span></div>
    <div class="color-square" style="background-color: #4b0c76;"><span class="color-label">Pretty Lilac</span></div>
    <div class="color-square" style="background-color: #AC5197;"><span class="color-label">Pink Heat</span></div>
    <div class="color-square" style="background-color: #5d0052;"><span class="color-label">Very Berry</span></div>
    <div class="color-square" style="background-color: #d37788;"><span class="color-label">Powerful Pink</span></div>
    <div class="color-square" style="background-color: #912644;"><span class="color-label">Passionate Red</span></div>
    <div class="color-square" style="background-color: #b61333;"><span class="color-label">Happy Red</span></div>
</div>

</body>
</html>
