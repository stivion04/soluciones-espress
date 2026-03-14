<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Soluciones Express | Servicio Técnico</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial, Helvetica, sans-serif;
}

body{
background:linear-gradient(135deg,#020617,#0f172a,#020617);
color:white;
}

/* HEADER */

header{
text-align:center;
padding:40px 20px;
background:#020617;
border-bottom:2px solid #38bdf8;
}

header img{
width:180px;
margin-bottom:15px;
}

header h1{
font-size:40px;
color:#38bdf8;
}

header p{
margin-top:10px;
color:#cbd5f5;
}

/* SERVICIOS */

.container{
padding:40px 20px;
text-align:center;
}

.container h2{
margin-bottom:30px;
color:#38bdf8;
}

.servicios{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
}

.card{
background:#1e293b;
padding:25px;
border-radius:12px;
transition:0.3s;
box-shadow:0 0 10px rgba(0,0,0,0.5);
}

.card:hover{
transform:translateY(-5px);
box-shadow:0 0 20px #38bdf8;
}

.card h3{
color:#38bdf8;
margin-bottom:10px;
}

/* FORMULARIO */

.formulario{
padding:40px 20px;
text-align:center;
background:#020617;
}

.formulario h2{
color:#38bdf8;
margin-bottom:20px;
}

form{
max-width:500px;
margin:auto;
display:flex;
flex-direction:column;
gap:15px;
}

input,select,textarea{
padding:12px;
border:none;
border-radius:8px;
font-size:15px;
}

textarea{
height:100px;
resize:none;
}

button{
background:#38bdf8;
color:white;
border:none;
padding:15px;
border-radius:8px;
font-size:16px;
cursor:pointer;
}

button:hover{
background:#0ea5e9;
}

/* CONTACTO */

.contacto{
padding:40px 20px;
text-align:center;
}

.mapa iframe{
width:90%;
max-width:800px;
height:350px;
border:0;
border-radius:10px;
margin-top:20px;
}

/* WHATSAPP */

.whatsapp{
position:fixed;
bottom:20px;
right:20px;
background:#25D366;
color:white;
font-size:28px;
padding:15px 18px;
border-radius:50%;
text-decoration:none;
box-shadow:0 0 10px rgba(0,0,0,0.4);
}

.whatsapp:hover{
background:#1ebe5d;
}

/* FOOTER */

footer{
text-align:center;
padding:20px;
background:#020617;
margin-top:40px;
color:#94a3b8;
}

</style>
</head>

<body>

<header>

<img src="logo.png">

<h1>Soluciones Express</h1>
<p>Servicio Técnico Profesional</p>
<p><b>Técnico: Dilan Camacho</b></p>

</header>

<section class="container">

<h2>Nuestros Servicios</h2>

<div class="servicios">

<div class="card">
<h3>Reparación de Impresoras</h3>
<p>Arreglo de impresoras Epson, HP y Canon.</p>
</div>

<div class="card">
<h3>Recarga de Cartuchos y Toner</h3>
<p>Recarga de cartuchos HP y toner para impresoras.</p>
</div>

<div class="card">
<h3>Reparación de Computadores</h3>
<p>Servicio técnico para computadores y portátiles.</p>
</div>

<div class="card">
<h3>Instalación de Programas</h3>
<p>Actualización de Windows, Office y todo tipo de programas.</p>
</div>

<div class="card">
<h3>Venta de Suministros</h3>
<p>Venta de tinta, toner y accesorios para impresoras y computadores.</p>
</div>

<div class="card">
<h3>Compra y Venta</h3>
<p>Compramos y vendemos computadores e impresoras.</p>
</div>

</div>

</section>

<section class="formulario">

<h2>Solicitar Servicio Técnico</h2>

<form id="serviceForm">

<input type="text" id="nombre" placeholder="Nombre completo" required>

<input type="tel" id="telefono" placeholder="Número de teléfono" required>

<select id="servicio">
<option>Reparación de impresora</option>
<option>Reparación de computador</option>
<option>Recarga de cartuchos</option>
<option>Recarga de toner</option>
<option>Instalación de programas</option>
<option>Mantenimiento</option>
</select>

<input type="text" id="direccion" placeholder="Dirección del servicio">

<textarea id="problema" placeholder="Describe el problema"></textarea>

<button type="submit">Enviar solicitud</button>

</form>

</section>

<section class="contacto">

<h2>Contacto</h2>

<p><b>Empresa:</b> Soluciones Express</p>
<p><b>Técnico:</b> Dilan Camacho</p>
<p><b>WhatsApp:</b> 3229148470</p>

<p><b>Dirección:</b><br>
Frente del CAI de Piamonte de Bosa<br>
Cra. 78c #69B-86 Sur<br>
Bosa, Bogotá, Cundinamarca
</p>

<div class="mapa">

<iframe 
src="https://www.google.com/maps?q=Cra+78c+69B-86+Sur+Bosa+Bogota&output=embed">
</iframe>

</div>

</section>

<footer>
© 2026 Soluciones Express | Dilan Camacho
</footer>

<a href="https://wa.me/573229148470?text=Hola%20quiero%20informacion%20sobre%20servicio%20tecnico" class="whatsapp" target="_blank">
💬
</a>

<script>

document.getElementById("serviceForm").addEventListener("submit", function(e){

e.preventDefault();

let nombre=document.getElementById("nombre").value;
let telefono=document.getElementById("telefono").value;
let servicio=document.getElementById("servicio").value;
let direccion=document.getElementById("direccion").value;
let problema=document.getElementById("problema").value;

let mensaje=`Hola quiero solicitar servicio técnico

Nombre: ${nombre}
Teléfono: ${telefono}
Servicio: ${servicio}
Dirección: ${direccion}
Problema: ${problema}`;

let url="https://wa.me/573229148470?text="+encodeURIComponent(mensaje);

window.open(url,"_blank");

});

</script>

</body>
</html>
