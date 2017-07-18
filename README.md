# vuejsRGB
<code>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>RGB</title>
     <!-- Compiled and minified CSS -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/0.99.0/css/materialize.min.css">

    <style>
        .color{
            margin: 150px 30px;
            /*background-color: rgb(0,255,200);*/
            min-height: 150px;
            width: 200px;
            border: 1px solid #585858;
        }
        p.prgb{
            margin-left: 30px;
        }
    </style>
    
</head>
<body>

<div class="container" id="app">
    <br>
    <div class="row">
        <div class="col s3 offset-s3">
            <p>Columna 1</p>
   
            <input type="number" min="1" max="255" step="1" placeholder="Red" v-model="red">
            <input type="range" min="0" max="255" step="1" v-model="red"><br><br>
            

            <input type="number" min="1" max="255" step="1" placeholder="Green" v-model="green">
            <input type="range" min="0" max="255" step="1" v-model="green"><br><br>

            <input type="number" min="1" max="255" step="1" placeholder="Blue" v-model="blue">
            <input type="range" min="0" max="255" step="1" v-model="blue"><br><br>
        </div>

        <div class="col s4">
            <p class="prgb">Color RGB: ({{parseInt(red)}}, {{parseInt(green)}}, {{parseInt(blue)}})</p>
            <div class="color" v-bind:style="{background: 'rgb('+parseInt(red)+','+parseInt(green)+','+parseInt(blue)+')'}">
            </div>
        </div>


    </div>
</div>


<script src="https://unpkg.com/vue"></script>

<script>
new Vue({
    el:'#app',
    data:{
        red:   255,
        green: 0,
        blue:  255,
    },
});
</script>

</body>
</html>
</code>
