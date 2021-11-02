<!DOCTYPE html>
<html dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Bread</title>
    <link rel="stylesheet" href="math.css">
  </head>
  <body>
    <div class="mina">
      <img src="math.jpg" class="fond">
      <header>
        <h1>MathMaster Tool</h1> <br>
      <h3>* Amadeo Jacohinde *</h3>
      </header>
      <div class="miLina">
      <div class="tallas">
        <div class="scri1" id="pan1">
<div class="disp">
  <input type="address" value="" placeholder="0" id="trada">
</div>
          <div class="botss">
            <div class="ols">
            <button type="button" class="ton" onclick="opio(1)"><h2>+</h2> </button>
            <button type="button" class="ton" onclick="opio(2)"><h2>-</h2></button>
            <button type="button" class="ton" onclick="opio(3)"><h2>*</h2></button>
            <button type="button" class="ton" onclick="opio(4)"><h2>%</h2></button>
          </div>
            <div class="oks">
              <div class="ojk">
              <button onclick="boti(1)">1</button>
              <button onclick="boti(2)">2</button>
              <button onclick="boti(3)">3</button>
              <button onclick="boti(4)">4</button>
              <button onclick="boti(5)">5</button>
              <button onclick="boti(6)">6</button>
              <button onclick="boti(7)">7</button>
              <button onclick="boti(8)">8</button>
              <button onclick="boti(9)">9</button>
              <button onclick="boto()">.</button>
              <button>0</button>
              <button onclick="limp()">AC</button>
            </div>
            <div style="background-color:grey;width:30%;">
              <button type="button" style="width:100%;min-height:6.7%" onclick="dela()"> &#8592; </button>
            <button type="button" class="ton2" id="iga" onclick="solv()"><h2>=</h2> </button>
            </div>
            </div>
          </div>
        </div>
        <div class="scri2" >
          <header id="talla2">
            <h3><u>Registro de Operaciones</u></h3><br>
            <p id="reg"></p>
          </header>

        </div>
      </div>
    </div>
    </div>
    <div class="dina">
      <header>
        <h1>Boxes</h1>
      </header>
      <p>This is the box #1</p>
      <p>Love</p>
    </div>
    <script type="text/javascript"> var lolo, resi, op1, op2;
    var di = 1;
var p = document.getElementById('trada');
var reg = document.getElementById('reg');
var relo = document.getElementById('talla2');

function dela(){
  var gea = document.getElementById('trada').value;
  document.getElementById('trada').value = gea.substring(-1, gea.length-1);
}
      function opio(v){
        var gea = document.getElementById('trada').value;
        lolo = v;
        p.value = "";
        var fe = document.createElement("P");
        switch (v) {
          case 1:
            p.placeholder = " + ";
            reg.innerHTML = gea + " + ";
            break;
          case 2:
              p.placeholder = " - ";
              reg.innerHTML = gea + " - ";
              break;
          case 3:
                p.placeholder = " * ";
                reg.innerHTML = gea + " * ";
                break;
          case 4:
                  p.placeholder = " / ";
                  reg.innerHTML = gea + " / ";
                  break;
        }
        op1 = gea;
        gea.onclick;
      }
function boti(e){
  document.getElementById('trada').value+= e;
}
function boto(){
  document.getElementById('trada').value += ".";
}
function limp(){
  document.getElementById('trada').value= "";
  p.placeholder="0";
}
function solv(){
   var tea = document.getElementById('trada').value;
   op2 = Number(tea);
   op1 = Number(op1);
   p.value = "";
   p.placeholder= "0";
   reg.innerHTML = "";
   var fe = document.createElement("P");
        switch (lolo) {
          case 1:
            resi = (op1 + op2);
            fe.innerHTML= di +") "+ op1 + " + " + op2 + " = " + resi;
            document.getElementById('talla2').appendChild(fe);
            di++;
            break;
          case 2:
          resi = (op1 - op2);
          fe.innerHTML= di +") "+ op1 + " - " + op2 + " = " + resi;
          document.getElementById('talla2').appendChild(fe);
          di++;
              break;
          case 3:
          resi = (op1 * op2);
          fe.innerHTML= di +") "+ op1 + " * " + op2 + " = " + resi;
          document.getElementById('talla2').appendChild(fe);
          di++;
                break;
          case 4:
          resi = (op1 / op2);
          fe.innerHTML= di +") "+ op1 + " / " + op2 + " = " + resi;
          document.getElementById('talla2').appendChild(fe);
          di++;
                  break;
        }
      }
    </script>
  </body>
</html>
