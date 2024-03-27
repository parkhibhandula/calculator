#First Github Repo
# calculator using javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        h1{
            text-align: center;
        }
        button{
            height: 40px;
            width: 40px;
        }
        #main{
            height: 40px;
            width: 200px;
        }
        #res{
          background-color: rgb(0, 110, 255);
          color: white;
        }
    </style>
</head>
<body>
    <script>
        function input(a){
            var y = document.getElementById("main").value+a;
            document.getElementById("main").value=y;
        }
        function result(a){
           var c= document.getElementById("main").value;
           document.getElementById("main").value = eval(c);
        }
        function clear1(){
            var x = document.getElementById("main").value
            x = x.slice(0,-1)
            document.getElementById("main").value = x
        }
        function clear2(){
            document.getElementById("main").value = " ";
        }
    </script>
    <div id="calc">
    <h1>CALCULATOR</h1>
        <tr>
            <td colspan="4"><input type="text" id="main"></td>
        </tr>
        <tr>
            <td><button onclick="input('%')">%</button></td>
            <td><button onclick="input('**')">^</button></td>
            <!-- <td><button onclick="input('3.14')">&Pi;</button></td> -->
            <td><button onclick="clear1()">C</button></td>
            <td><button onclick="clear2()">AC</button></td>
                </tr>
        <tr>
            <td><button onclick="input('7')">7</button></td>
            <td><button onclick="input('8')">8</button></td>
            <td><button onclick="input('9')">9</button></td>
            <td><button onclick="input('*')">x</button></td>
        </tr>
        <tr>
            <td><button onclick="input('6')">6</button></td>
            <td><button onclick="input('5')">5</button></td>
            <td><button onclick="input('4')">4</button></td>
            <td><button onclick="input('-')">-</button></td>
        </tr>
        <tr>
            <td><button onclick="input('1')">1</button></td>
            <td><button onclick="input('2')">2</button></td>
            <td><button onclick="input('3')">3</button></td>
            <td><button onclick="input('+')">+</button></td>
        </tr>
        <tr>
            <td><button onclick="input('0')">0</button></td>
            <td><button onclick="input('.')">.</button></td>
            <td><button onclick="input('/')">/</button></td>
            <td><button onclick="result()" id="res">=</button></td>
        </tr>
    </table>
    <!-- <iframe width="800" height="800" src="https://www.youtube.com/embed/q06-jtY_yzQ" title="AKTU EXAM | COA KCS302| floating point addition and subtraction with flowchart |LS Academy" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe> -->
</div>
</body>
</html>
