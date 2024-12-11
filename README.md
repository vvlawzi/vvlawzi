<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beating Heart</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background-color: #f5f5f5;
        }

        .heart {
            position: relative;
            width: 100px;
            height: 100px;
            background-color: red;
            transform: rotate(-45deg);
            animation: beat 1s infinite;
        }

        .heart:before,
        .heart:after {
            content: "";
            position: absolute;
            width: 100px;
            height: 100px;
            background-color: red;
            border-radius: 50%;
        }

        .heart:before {
            top: -50px;
            left: 0;
        }

        .heart:after {
            left: 50px;
            top: 0;
        }

        @keyframes beat {
            0%, 20%, 50%, 80%, 100% {
                transform: scale(1) rotate(-45deg);
            }
            40% {
                transform: scale(1.2) rotate(-45deg);
            }
            60% {
                transform: scale(0.9) rotate(-45deg);
            }
        }
    </style>
</head>
<body>
    <div class="heart"></div>
</body>
</html>

