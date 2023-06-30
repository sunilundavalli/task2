<!DOCTYPE html>
<html lang="en">

<head>
    <style>
        * {
            padding: 0;
            margin: 0;
            font-family: 'poppins', calibri;
        }

        body {
            background-color: #495250;
            display: grid;
            height: 100vh;
            place-items: center;
        }

        .main {
            width: 400px;
            height: 450px;
            background-color: black;
            position: absolute;
            border: 6px  grey;
            border-radius: 7px;
        }

        .main input[type='text'] {
            width: 88%;
            position: relative;
            height: 88px;
            top: 10px;
            text-align: right;
            padding: 3px 6px;
            outline: none;
            font-size: 40px;
            border: 5px black;
            display: flex;
            margin: auto;
            border-radius: 10px;
            color: black;
        }

        .btn input[type='button'] {
            width: 90px;
            padding: 2px;
            margin: 2px 0px;
            position: relative;
            left: 13px;
            top: 20px;
            height: 60px;
            cursor: pointer;
            font-size: 18px;
            transition: 0.5s;
            background-color: #495250;
            border-radius: 6px;
            color: black;
        }

        .btn input[type='button']:hover {
            background-color: green;
            color: black;
        }
    </style>
    <script>
        function Solve(val) {
            var v = document.getElementById('res');
            v.value += val;
        }

        function Result() {
            var num1 = document.getElementById('res').value;
            var num2 = eval(num1);
            document.getElementById('res').value = num2;
        }

        function Clear() {
            var inp = document.getElementById('res');
            inp.value = '';
        }

        function green() {
            var ev = document.getElementById('res');
            ev.value = ev.value.slice(0, -1);
        }
    </script>
    <title>Calulator</title>
</head>

<body>
    <div class="main">
        <input type="text" id='res'>
        <div class="btn">
            <input type="button" value='C' onclick="Clear()">
            <input type="button" value='%' onclick="Solve('%')">
            <input type="button" value='←' onclick="Back('←')">
            <input type="button" value='/' onclick="Solve('/')">
            <br>
            <input type="button" value='7' onclick="Solve('7')">
            <input type="button" value='8' onclick="Solve('8')">
            <input type="button" value='9' onclick="Solve('9')">
            <input type="button" value='x' onclick="Solve('*')">
            <br>
            <input type="button" value='4' onclick="Solve('4')">
            <input type="button" value='5' onclick="Solve('5')">
            <input type="button" value='6' onclick="Solve('6')">
            <input type="button" value='-' onclick="Solve('-')">
            <br>
            <input type="button" value='1' onclick="Solve('1')">
            <input type="button" value='2' onclick="Solve('2')">
            <input type="button" value='3' onclick="Solve('3')">
            <input type="button" value='+' onclick="Solve('+')">
            <br>
            <input type="button" value='00' onclick="Solve('00')">
            <input type="button" value='0' onclick="Solve('0')">
            <input type="button" value='.' onclick="Solve('.')">
            <input type="button" value='=' onclick="Result()">
        </div>
    </div>
    <script src='Calc.js'></script>
</body>

</html>
