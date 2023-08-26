---
layout: page
title: Juzo
permalink: /juzo/
---
<!DOCTYPE html>
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
            
        }

.color-label {
    position: absolute;
    color: white;
    font-weight: bold;
    font-size: 16px; /* Adjust this value as needed */
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
            {name: "Pinky", code: "#F2B5D4"},
            {name: "Magenta", code: "#FF00FF"},
            {name: "Red", code: "#FF0000"},
            {name: "Orange", code: "#FFA500"},
            {name: "Yellow", code: "#FFFF00"},
            {name: "Green", code: "#008000"},
            {name: "Blue", code: "#0000FF"},
            {name: "Indigo", code: "#4B0082"},
            {name: "Violet", code: "#EE82EE"},
            {name: "Black", code: "#000000"},
            {name: "White", code: "#FFFFFF"},
            {name: "Gray", code: "#808080"},
            {name: "Goldenrod", code: "#DAA520"},
            {name: "Aquamarine", code: "#7FFFD4"},
            {name: "Teal", code: "#008080"},
            {name: "Lime", code: "#00FF00"},
            {name: "Khaki", code: "#F0E68C"},
            {name: "Salmon", code: "#FA8072"},
            {name: "Plum", code: "#DDA0DD"},
            {name: "Periwinkle", code: "#CCCCFF"},
            {name: "Olive", code: "#808000"},
            {name: "Navy", code: "#000080"},
            {name: "Mint", code: "#3EB489"},
            {name: "Coral", code: "#FF7F50"},
            {name: "Chocolate", code: "#D2691E"},
            {name: "Charcoal", code: "#36454F"},
            {name: "Beige", code: "#F5F5DC"},
            {name: "Azure", code: "#007FFF"},
            {name: "Amber", code: "#FFBF00"},
            {name: "Crimson", code: "#DC143C"},
            {name: "Emerald", code: "#50C878"},
            {name: "Jade", code: "#00A86B"},
            {name: "Lavender", code: "#B57EDC"},
            {name: "Mustard", code: "#FFDB58"},
            {name: "Rose", code: "#FF007F"},
            {name: "Turquoise", code: "#40E0D0"},
            {name: "Bisque", code: "#FFE4C4"},
            {name: "Burgundy", code: "#800020"},
            {name: "Fuchsia", code: "#FF00FF"},
            {name: "Ivory", code: "#FFFFF0"},
            {name: "Lilac", code: "#C8A2C8"},
            {name: "Gold", code: "#FFD700"},
            {name: "Rust", code: "#B7410E"},
            {name: "Silver", code: "#C0C0C0"},
            {name: "Taupe", code: "#483C32"},
            {name: "Pear", code: "#D1E231"},
            {name: "Apricot", code: "#FBCEB1"},
            {name: "Bronze", code: "#CD7F32"},
            {name: "Cola", code: "#3E2723"},
            {name: "Ruby", code: "#E0115F"},
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
