<!DOCTYPE html>
<html>
<head>
    <title>Pseudo Elements and Pseudo Classes</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color:#f9edbd;
        }
        .container {
            width: 800px;
            margin: 40px auto;
            text-align: center;
        }
        .box {
            width: 200px;
            height: 200px;
            background-color: #bdf9e8;
            margin: 20px;
            display: inline-block;
            position: relative;
            cursor:pointer;
        }
        .box::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color:#90ff8e;
            transform: scale(0);
            transition: transform 0.3s ease-in-out;
        }
        .box:hover::before {
            transform: scale(1);
        }
        .box:active::before {
            background-color:#60fff1; 
        }
        .box:focus::before {
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        }
        .box:nth-child(2n+1) {
            background-color: #8effb9;
        }
        .box:nth-child(2n+1)::before {
            background-color: #8ef7ff;
        }
        .button {
            background-color: #007bff;
            color: #ffffff;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border-radius:4px;
            margin:30px;
        }
        .button:hover {
            background-color: #7fff96;
            color:black;
        }
        .button:active {
            background-color: #ffaa60;
        }
        .button:focus {
            box-shadow: 0 2 10px rgba(0, 0, 0, 0.5);
        }
    </style>
    
</head>
<body>
    <div class="container">
        <h1>Pseudo Elements and Pseudo Classes</h1>
        <div class="box">Box 1</div>
        <div class="box">Box 2</div>
        <div class="box">Box 3</div>

        <button class="button">Hover me!</button>
        <button class="button">Click me!</button>
        
        <input type="text" placeholder="Focus me!"><br>
        
        <div class="box">Box 1</div>
        <div class="box">Box 2</div>
        <div class="box">Box 3</div>
        <div class="box">Box 4</div>
        <div class="box">Box 5</div>
    </div>
</body>
</html>
