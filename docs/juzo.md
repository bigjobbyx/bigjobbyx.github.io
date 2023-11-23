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
            margin: 0px;
        }

        .color-grid {
            display: grid;
            grid-template-columns: repeat(1, 1fr);
            gap: 0px;
        }

        @media (orientation: landscape) {
            .color-grid {
                grid-template-columns: repeat(3, 1fr);
            }
        }

        .color-box {
            position: relative;
            height: 150px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

.color-label {
    position: absolute;
    color: white;
    font-weight: bold;
    text-shadow: -1px -1px 0 #000,  
                 1px -1px 0 #000,
                 -1px 1px 0 #000,
                 1px 1px 0 #000;
}
    </style>
</head>
<body>
    <div class="color-grid">
        <!-- Colors will be populated here by the script -->
    </div>

    <script>
        // List of colors
        let colors = [
            {name: "Black pepper", code: "#000000"},
            {name: "White", code: "#ffffff"},
            {name: "Light Grey", code: "#DEDEDE"},
 
            {name: "Pearl", code: "#9f8277"},
            {name: "Coffee creme", code: "#958072"},
            {name: "Sandel", code: "#ceb5a1"},
            {name: "Cacao", code: "#664e40"},
            {name: "Make-Up", code: "#cdb09f"},
            {name: "Beige", code: "#D0B4A6"},
            {name: "Sepia", code: "#A59B8F"},
            {name: "Cashmere", code: "#A48F70"},
            {name: "Cardamom", code: "#d0bca6"},
            {name: "Silk", code: "#b7a090"},
            {name: "Sand", code: "#C5BEB4"},
            {name: "Unique Taupe", code: "#867c6b"},
            {name: "Smoke", code: "#776546"},
            {name: "Almond", code: "#c2b19e"},
            {name: "Sesame", code: "#d5c8b2"},
            {name: "Light beige", code: "#d5c8b2"},
            {name: "Anise", code: "#9a7d66"},
            {name: "Nutmeg", code: "#a4917b"},
            {name: "Smooth Olive", code: "#aea40c"},
            {name: "Glowing Green", code: "#57A434"},
            {name: "Stunning Green", code: "#b1ceb3"},
            {name: "Deep Aqua", code: "#257b80"},
            {name: "Ionic Blue", code: "#0384BB"},
            {name: "Mellow Blue", code: "#9fc4d6"},
            {name: "Awesome Blue", code: "#7694b6"},
            {name: "Blueberry", code: "#254377"},
            {name: "Dark Blue Sensation", code: "#254290"},
            {name: "Dark blue", code: "#161F62"},
            {name: "Navy", code: "#08112F"},
            {name: "Marine (FR)", code: "#06092A"},
            {name: "Marine", code: "#08112F"},
            {name: "Night Blue", code: "#2e2c52"},
            {name: "Juniper", code: "#06092a"},
            {name: "Romance", code: "#2E2635"},
            {name: "Purple Lightning", code: "#3B2762"},
            {name: "Pretty Lilac", code: "#4b0c76"},
            {name: "Pink Heat", code: "#AC5197"},
            {name: "Very Berry", code: "#5d0052"},
            {name: "Powerful Pink", code: "#d37788"},
            {name: "Passionate Red", code: "#912644"},
            {name: "Happy Red", code: "#b61333"},

        ];

        let grid = document.querySelector(".color-grid");
        
        colors.forEach(color => {
            let box = document.createElement("div");
            box.className = "color-box";
            box.style.backgroundColor = color.code;

            let label = document.createElement("span");
            label.className = "color-label";
            label.innerText = color.name;

            box.appendChild(label);
            grid.appendChild(box);
        });
    </script>
</body>
</html>
.
