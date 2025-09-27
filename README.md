# machine

<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Conversão de Bases</title>
    <link rel="shortcut icon" href="https://raw.githubusercontent.com/AssisJP06/machine/refs/heads/main/machine01/calculadora.ico" type="image/x-icon">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@300..700&display=swap');

        @import url('https://fonts.googleapis.com/css2?family=Source+Code+Pro:wght@300..900&display=swap');

        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;700&display=swap');

        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap');

        @font-face {

            font-family: 'android';
            src: url('https://raw.githubusercontent.com/AssisJP06/machine/main/machine01/idroid.otf') format('opentype');
            font-weight: normal;
        }

        body {

            height: 100%;
            display: flex;
            flex-direction: column;

            background-image: url('https://github.com/AssisJP06/machine/blob/main/machine01/unnamed.png?raw=true');

            background-color: #5570c752;

            background-position: center center;
            background-attachment: fixed;
            background-size: cover;
            background-repeat: no-repeat;
            margin: 0px;
            padding: 0px;


            font-family: Arial, Helvetica, sans-serif;


        }

        header {
            display: flex;
            justify-content: center;
            background-color: rgba(0, 0, 0, 0.911);
            border-bottom: 3px solid #266eeb;
            height: 130px;


        }

        header>h1 {
            font-family: 'android';
            color: white;
            padding-bottom: 35px;
            font-weight: lighter;
            font-size: 50px;

        }

        #container {

            display: flex;
            
            justify-content: space-evenly;
            width: 100%;
            height: 100%;
        }

        .calculadora {

            width: 500px;
            height: 100%;

            border-radius: 5%;

            margin-top: 80px;

            background-color: #5570c7dc;

            overflow: hidden;

            display: flex;
            align-items: center;
            flex-direction: column;
            justify-content: center;

            box-shadow: 3px 5px 20px rgba(59, 88, 205, 0.536);

        }

        h2 {
            margin: auto auto 10px auto;
            color: rgba(0, 0, 0, 0.79);
            font-size: 30px;
            width: 100%;
            text-align: center;
            background-color: rgba(255, 255, 255, 0.71);
            border: 1px solid white;
            margin-top: 0px;
            padding: 13px;
            font-family: Poppins;
            font-weight: bolder;
            letter-spacing: 1px;

        }

        h3 {

            color: white;
            font-size: 19px;
            font-weight: lighter;
            font-family: Poppins;
        }

        select {
            text-align: center;
            padding: 5px;
            cursor: pointer;
            border-radius: 10px;
            font-size: 16px;
            font-family: 'Source Code Pro';
            border: 1px solid #c9d6ff;
        }

        input {
            border-radius: 10px;
            padding: 5px;
            font-size: 16px;
            margin-bottom: 10px;
            font-family: 'Source Code Pro';
            text-align: center;
            border: 1px solid #c9d6ff;

        }

        input:focus {
            outline: none;
            box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
        }

        label {
            margin: 15px 0px;
            color: white;
            font-weight: lighter;
            font-size: 18px;
            cursor: pointer;
            font-family: Poppins;

        }

        button {
            padding: 12px 25px;
            margin: 15px;

            border-radius: 10px;
            border: none;

            background-color: #293d9f;
            color: white;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);

            font-weight: bold;
            font-family: Montserrat;


            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #3b4582;
            transform: translateY(-2px);
        }

        #div_resposta {

            display: none;

            flex-direction: column;
            align-items: center;
            justify-content: center;

            background-color: #5570c7e6;
            overflow: hidden;

            height: 100%;
            width: 400px;
            margin-top: 60px;

            border-radius: 5%;
            box-shadow: 3px 5px 20px rgba(59, 88, 205, 0.536);


        }



        #div_resposta p {
            margin: 10px 0px;
            font-size: 20px;
            color: rgba(0, 0, 0, 0.896);
            font-weight: normal;
            font-family: Poppins, sans-serif;
            line-height: 1.5;
            
        }
        .primeiro{
            margin-top: 0px;
        }

        span {
            font-size: 18px;
            color: #d9e2ff;
            border-radius: 5px;
            font-weight: bold;
            font-family: 'Roboto';
            margin-bottom: 5px;


        }
        #div_resposta div{
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        #div_resposta div:last-child{
            border: none;
        }

        #cor1{
            border-bottom: 3px solid rgba(55, 239, 168, 0.601);
        }
        #cor2{
            border-bottom: 3px solid rgba(86, 23, 233, 0.634);
        }
        #cor3{
            border-bottom: 3px solid rgba(55, 239, 168, 0.601);}

        .ultimo {
            margin-bottom: 10px;
        }
        footer {
            
            display: flex;
            flex-direction: column;
            align-items: center;
            
            
            

            width: 100%;
            
            position: relative;
            bottom: -50px;

            padding: 13px 0; 
            background-color: #0e1937f4;
            color: #fff; 
            font-family: 'Poppins', sans-serif; 
            font-size: 12px; 
            border-top: 1px solid #1a1a1a;
            margin-top: 50px;
            
            
}

footer p {
    margin: 3px 0px; 
    
}

    </style>

</head>

<body>
    <header>

        <h1>SPTecher's Machine</h1>

    </header>
    <div id="container">
        <div class="calculadora">
            <h2>Calculadora De Base</h2>
            <h3>Escolha a base de conversão</h3>
            <select id="numerico">
                <option value="0" selected disabled class="op0">Selecione a opção</option>
                <option value="1">Octal</option>
                <option value="2">Binário</option>
                <option value="3">Hexadecimal</option>
                <option value="4">Decimal</option>
            </select>
            <label for="input_n">Digite um número / letra</label>
            <input type="text" id="input_n" placeholder="Insira o número">

            <button onclick="calcular()">Calcular</button>


        </div>
        <div id="div_resposta">

        </div>
        

    </div>
    <footer>
    <p>&copy; 2025 SPTECHER'S MACHINE. Todos os direitos reservados.</p>
    <p>Desenvolvido por João Pedro Assis</p>
</footer>
</body>

</html>
<script>
    function calcular() {

        var base = numerico.value;
        var numero = input_n.value.trim();

        // Fazendo a validação dos números digitados

        div_resposta.style.display = 'flex';



        if (base == "4" && !/^[0-9]+$/.test(numero)) {
            alert("Digite apenas números de 0 a 9");
            div_resposta.style.display = 'none';
            return;

        }
        if (base == "1" && !/^[0-7]+$/.test(numero)) {
            alert("Digite apenas números de 0 a 7");
            div_resposta.style.display = 'none';
            return;

        }
        if (base == "2" && !/^[01]+$/.test(numero)) {
            alert("Digite apenas 0 ou 1");
            div_resposta.style.display = 'none';
            return;

        }
        if (base == "3" && !/^[0-9A-Fa-f]+$/.test(numero)) {
            alert("Digite apenas números de 0 a 9 e letras de A a F");
            div_resposta.style.display = 'none';
            return;

        }
        if (base == '4') {
            numero = Number(numero);
        }

        else if (base == '1') {
            numero = parseInt(numero, 8);
        }

        else if (base == '3') {
            numero = parseInt(numero, 16);
        }

        else {
            numero = parseInt(numero, 2);
        }
        if (base != '2' && base != '3' && base != '4' && base != '1') {
            alert('Escolha uma base');
            div_resposta.style.display = 'none';
            return;
        }

        else {

            div_resposta.innerHTML = `
            <h2>Convertido</h2>
                <div id = 'cor1'>
                    <p id='decimal' class ='primeiro'>Decimal</p> <span>${numero.toString(10)}</span>
                </div>
            
                <div id ='cor2'>
                    <p id='hexadecimal'>Hexadecimal </p><span>${numero.toString(16).toUpperCase()}</span>
                </div>
           
                
                <div id ='cor3'>
                    <p id='binario'>Binário</p><span> ${numero.toString(2)}</span>
                </div>
                
            
            <div id ='cor4'>
                <p id='octal'>Octal</p> <span class = 'ultimo'>${numero.toString(8)}</span>
            </div>
        `;


            decimal.style.display = 'none';
            octal.style.display = 'none';
            binario.style.display = 'none'; hexadecimal.style.display = 'none';




            if (base != 'Decimal') {
                decimal.style.display = 'flex';


            }

            if (base != 'Octal') {
                octal.style.display = 'flex';
            }

            if (base != 'Hexadecimal') {
                hexadecimal.style.display = 'flex';
            }

            if (base != 'Binário') {
                binario.style.display = 'flex';
            }

        }

    }
</script>
