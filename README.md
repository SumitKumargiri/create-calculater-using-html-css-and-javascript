# create-calculater-using-html-css-and-javascript

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>claculater</title>
</head>
<style>
    body {
        height: 100%;
        width: 100%;
    }

    .button {
        width: 66px;
        padding: 20px;
        margin: 0px 3px;
        border: 2px solid black;
        border-radius: 9px;
        cursor: pointer;
    }

    h1 {
        text-align: center;
    }

    .row {
        text-align: center;
        margin: 8px 0px;
    }

    #row input {
        margin: 0px
    }

    .input {
        padding: 10px 68px;
        margin: 0px;
        border-radius: 8px;
        border: 2px solid black;
    }
</style>

<body>
    <h1>calculater using html, css and javascript</h1>
    <div class="row" id="row">
        <input class="input" type="text">
    </div>

    <div class="container">
        <div class="row">
            <button class="button">c</button>
            <button class="button">M+</button>
            <button class="button">M-</button>
            <button class="button">%</button>
        </div>

        <div class="row">
            <button class="button">7</button>
            <button class="button">8</button>
            <button class="button">9</button>
            <button class="button">*</button>
        </div>

        <div class="row">
            <button class="button">4</button>
            <button class="button">5</button>
            <button class="button">6</button>
            <button class="button">/</button>
        </div>

        <div class="row">
            <button class="button">1</button>
            <button class="button">2</button>
            <button class="button">3</button>
            <button class="button">+</button>
        </div>

        <div class="row">
            <button class="button">0</button>
            <button class="button">.</button>
            <button class="button">=</button>
            <button class="button">-</button>
        </div>
    </div>
</body>
<script>
    let string = "";
    let buttons = document.querySelectorAll('.button');
    Array.from(buttons).forEach((button) => {
        button.addEventListener('click', (e) => {
            if (e.target.innerHTML == '=') {
                string = eval(string);
                document.querySelector('input').value = string;

            }
            else if (e.target.innerHTML == 'c') {
                string = " ";
                document.querySelector('input').value = string;

            } else {
                console.log(e.target);
                string = string + e.target.innerHTML;
                document.querySelector('input').value = string;
            }
        })
    })
</script>

</html>


#  output:-

![image](https://user-images.githubusercontent.com/96234273/220813828-fcebdf94-9a34-4666-930b-f05db2fe3fc8.png)
