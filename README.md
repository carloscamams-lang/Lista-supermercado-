<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Lista de Compras</title>

<style>
body{
font-family:Arial;
background:#f2f2f2;
padding:20px;
}

h1{
text-align:center;
}

.item{
background:white;
padding:12px;
margin:6px 0;
border-radius:8px;
font-size:20px;
}

.checked{
text-decoration:line-through;
color:gray;
}

button{
margin-top:20px;
padding:12px;
font-size:16px;
}
</style>
</head>

<body>

<h1>🛒 Lista de Supermercado</h1>

<div class="item"><input type="checkbox" id="1"> Arroz</div>
<div class="item"><input type="checkbox" id="2"> Feijão</div>
<div class="item"><input type="checkbox" id="3"> Macarrão</div>
<div class="item"><input type="checkbox" id="4"> Trigo (2)</div>
<div class="item"><input type="checkbox" id="5"> Granola</div>
<div class="item"><input type="checkbox" id="6"> Granulado colorido</div>
<div class="item"><input type="checkbox" id="7"> Frango (5)</div>
<div class="item"><input type="checkbox" id="8"> Requeijão (2)</div>
<div class="item"><input type="checkbox" id="9"> Manteiga (2)</div>
<div class="item"><input type="checkbox" id="10"> Margarina (2)</div>
<div class="item"><input type="checkbox" id="11"> Molho (2)</div>
<div class="item"><input type="checkbox" id="12"> Café (3)</div>
<div class="item"><input type="checkbox" id="13"> Milho de pipoca</div>
<div class="item"><input type="checkbox" id="14"> Pizza</div>
<div class="item"><input type="checkbox" id="15"> Pão de queijo</div>
<div class="item"><input type="checkbox" id="16"> Ovos</div>
<div class="item"><input type="checkbox" id="17"> Leite em pó</div>
<div class="item"><input type="checkbox" id="18"> Leite desnatado</div>
<div class="item"><input type="checkbox" id="19"> Água com gás</div>

<h2>Higiene</h2>

<div class="item"><input type="checkbox" id="20"> Detergente (4)</div>
<div class="item"><input type="checkbox" id="21"> Sabonete (4)</div>
<div class="item"><input type="checkbox" id="22"> Sabonete Meninos (3)</div>
<div class="item"><input type="checkbox" id="23"> Sabonete líquido Meninos</div>
<div class="item"><input type="checkbox" id="24"> Creme dental</div>
<div class="item"><input type="checkbox" id="25"> Creme dental Meninos</div>
<div class="item"><input type="checkbox" id="26"> Enxague bucal</div>
<div class="item"><input type="checkbox" id="27"> Desodorante</div>
<div class="item"><input type="checkbox" id="28"> Papel higiênico</div>
<div class="item"><input type="checkbox" id="29"> Papel toalha</div>
<div class="item"><input type="checkbox" id="30"> Vinagre</div>
<div class="item"><input type="checkbox" id="31"> Bicarbonato</div>
<div class="item"><input type="checkbox" id="32"> Lysoform</div>
<div class="item"><input type="checkbox" id="33"> Saco para lixo</div>
<div class="item"><input type="checkbox" id="34"> Veneno</div>

<button onclick="limpar()">Limpar lista</button>

<script>

const boxes=document.querySelectorAll("input");

boxes.forEach(box=>{

let saved=localStorage.getItem(box.id);

if(saved==="true"){
box.checked=true;
box.parentElement.classList.add("checked");
}

box.addEventListener("change",()=>{

localStorage.setItem(box.id,box.checked);

if(box.checked){
box.parentElement.classList.add("checked");
}else{
box.parentElement.classList.remove("checked");
}

});

});

function limpar(){

localStorage.clear();
location.reload();

}

</script>

</body>
</html>
