<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Encanto de Cacau</title>

<link rel="stylesheet"
href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"/>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{
    background:#0f0f0f;
    color:white;
}

/* MENU */

header{
    background:#161616;
    padding:18px 40px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    position:sticky;
    top:0;
    z-index:1000;
    border-bottom:1px solid #2a2a2a;
}

.logo{
    font-size:30px;
    font-weight:bold;
    color:#ffb347;
}

.menu{
    display:flex;
    gap:15px;
}

.menu button{
    padding:10px 18px;
    border:none;
    border-radius:12px;
    background:#ffb347;
    color:#111;
    font-weight:bold;
    cursor:pointer;
}

/* BANNER */

.banner{
    height:420px;
    background:
    linear-gradient(rgba(0,0,0,0.6),
    rgba(0,0,0,0.7)),
    url("https://images.unsplash.com/photo-1511381939415-e44015466834");
    background-size:cover;
    background-position:center;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
}

.banner .texto{
    background:rgba(20,20,20,0.7);
    padding:35px;
    border-radius:25px;
}

.banner h1{
    font-size:55px;
    color:#ffb347;
    margin-bottom:15px;
}

.banner p{
    font-size:20px;
    color:#ddd;
}

/* PESQUISA */

.barra{
    max-width:600px;
    margin:35px auto;
    padding:0 20px;
}

.barra input{
    width:100%;
    padding:18px;
    border:none;
    border-radius:15px;
    background:#1e1e1e;
    color:white;
    font-size:16px;
    border:1px solid #333;
}

/* CATEGORIAS */

.categorias{
    display:flex;
    gap:15px;
    overflow-x:auto;
    padding:10px 20px 30px;
}

.categoria{
    background:#1e1e1e;
    padding:12px 20px;
    border-radius:15px;
    border:1px solid #333;
    white-space:nowrap;
    cursor:pointer;
}

.categoria:hover{
    border-color:#ffb347;
    color:#ffb347;
}

/* PRODUTOS */

#produtos{
    padding:20px;
}

.container{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:25px;
}

.card{
    background:#1a1a1a;
    border-radius:22px;
    overflow:hidden;
    border:1px solid #2f2f2f;
    transition:0.3s;
}

.card:hover{
    transform:translateY(-6px);
    border-color:#ffb347;
}

.galeria{
    display:flex;
    overflow-x:auto;
    gap:10px;
    padding:15px;
}

.miniatura{
    width:120px;
    height:120px;
    object-fit:cover;
    border-radius:15px;
    flex-shrink:0;
}

.info{
    padding:20px;
}

.info h2{
    margin-bottom:10px;
}

.preco{
    color:#ffb347;
    font-size:28px;
    font-weight:bold;
    margin-bottom:15px;
}

.upload{
    width:100%;
    padding:12px;
    border-radius:12px;
    background:#111;
    color:#ccc;
    border:1px solid #333;
    margin-bottom:15px;
}

.botoes{
    display:flex;
    gap:10px;
}

.botao{
    flex:1;
    padding:15px;
    border:none;
    border-radius:14px;
    background:#ffb347;
    color:#111;
    font-size:15px;
    font-weight:bold;
    cursor:pointer;
}

.favorito{
    width:55px;
    border:none;
    border-radius:14px;
    background:#222;
    color:#ff4d6d;
    font-size:20px;
    cursor:pointer;
}

/* CARRINHO */

#carrinho{
    background:#1a1a1a;
    margin-top:45px;
    padding:30px;
    border-radius:25px;
    border:1px solid #2f2f2f;
}

#listaCarrinho li{
    margin:12px 0;
}

.total{
    margin-top:20px;
    font-size:30px;
    color:#ffb347;
    font-weight:bold;
}

.finalizar input{
    width:100%;
    padding:15px;
    margin-top:15px;
    border:none;
    border-radius:12px;
    background:#111;
    color:white;
    border:1px solid #333;
}

/* FOOTER */

footer{
    margin-top:50px;
    background:#161616;
    color:#aaa;
    text-align:center;
    padding:30px;
}

</style>
</head>

<body>

<header>

<div class="logo">
🍫 Encanto de Cacau
</div>

<div class="menu">
<button>Início</button>
<button>Produtos</button>
<button>Carrinho</button>
</div>

</header>

<!-- BANNER -->

<div class="banner">

<div class="texto">

<h1>Loja Premium 🎁</h1>

<p>
Presentes especiais para momentos especiais
</p>

</div>

</div>

<!-- PESQUISA -->

<div class="barra">

<input
type="text"
id="pesquisa"
placeholder="Pesquisar produtos..."
onkeyup="pesquisarProduto()"
>

</div>

<!-- CATEGORIAS -->

<div class="categorias">

<div class="categoria">🍫 Chocolates</div>

<div class="categoria">🎁 Presentes</div>

<div class="categoria">🧸 Ursos</div>

<div class="categoria">🌹 Flores</div>

<div class="categoria">☕ Cestas</div>

<div class="categoria">💎 Premium</div>

<div class="categoria">🔥 Promoções</div>

</div>

<!-- PRODUTOS -->

<section id="produtos">

<div class="container">

<!-- CARD -->

<div class="card">

<div class="galeria">

<img class="miniatura"
src="https://images.unsplash.com/photo-1511381939415-e44015466834">

<img class="miniatura"
src="https://images.unsplash.com/photo-1541781774459-bb2af2f05b55">

</div>

<div class="info">

<h2>Chocolate Premium</h2>

<p class="preco">
R$ 45
</p>

<input
class="upload"
type="file"
multiple
onchange="trocarVariasImagens(event,this)"
>

<div class="botoes">

<button
class="botao"
onclick="adicionarCarrinho('Chocolate Premium',45)">
<i class="fa-solid fa-cart-shopping"></i>
Comprar
</button>

<button class="favorito">
❤
</button>

</div>

</div>

</div>

<!-- CARD -->

<div class="card">

<div class="galeria">

<img class="miniatura"
src="https://images.unsplash.com/photo-1563901935883-cb33a4f3d1dd">

<img class="miniatura"
src="https://images.unsplash.com/photo-1517841905240-472988babdf9">

</div>

<div class="info">

<h2>Urso Especial</h2>

<p class="preco">
R$ 70
</p>

<input
class="upload"
type="file"
multiple
onchange="trocarVariasImagens(event,this)"
>

<div class="botoes">

<button
class="botao"
onclick="adicionarCarrinho('Urso Especial',70)">
<i class="fa-solid fa-cart-shopping"></i>
Comprar
</button>

<button class="favorito">
❤
</button>

</div>

</div>

</div>

<!-- CARD -->

<div class="card">

<div class="galeria">

<img class="miniatura"
src="https://images.unsplash.com/photo-1515934751635-c81c6bc9a2d8">

<img class="miniatura"
src="https://images.unsplash.com/photo-1509042239860-f550ce710b93">

</div>

<div class="info">

<h2>Cesta Luxo</h2>

<p class="preco">
R$ 150
</p>

<input
class="upload"
type="file"
multiple
onchange="trocarVariasImagens(event,this)"
>

<div class="botoes">

<button
class="botao"
onclick="adicionarCarrinho('Cesta Luxo',150)">
<i class="fa-solid fa-cart-shopping"></i>
Comprar
</button>

<button class="favorito">
❤
</button>

</div>

</div>

</div>

<!-- CARD -->

<div class="card">

<div class="galeria">

<img class="miniatura"
src="https://images.unsplash.com/photo-1490750967868-88aa4486c946">

<img class="miniatura"
src="https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9">

</div>

<div class="info">

<h2>Kit Flores</h2>

<p class="preco">
R$ 95
</p>

<input
class="upload"
type="file"
multiple
onchange="trocarVariasImagens(event,this)"
>

<div class="botoes">

<button
class="botao"
onclick="adicionarCarrinho('Kit Flores',95)">
<i class="fa-solid fa-cart-shopping"></i>
Comprar
</button>

<button class="favorito">
❤
</button>

</div>

</div>

</div>

</div>

<!-- CARRINHO -->

<div id="carrinho">

<h2>
🛒 Seu Carrinho
</h2>

<ul id="listaCarrinho"></ul>

<div class="total">
Total: R$ <span id="total">0</span>
</div>

<div class="finalizar">

<input
type="text"
id="endereco"
placeholder="Seu endereço"
>

<input
type="text"
id="telefone"
placeholder="Seu telefone"
>

<button
class="botao"
onclick="finalizarPedido()">
Finalizar Pedido
</button>

</div>

</div>

</section>

<footer>
© 2026 Encanto de Cacau
</footer>

<script>

/* GALERIA */

function trocarVariasImagens(event,elemento){

    const arquivos = event.target.files;

    const galeria =
    elemento.parentElement.previousElementSibling;

    for(let i = 0; i < arquivos.length; i++){

        const leitor = new FileReader();

        leitor.onload = function(e){

            const img =
            document.createElement("img");

            img.src = e.target.result;

            img.className = "miniatura";

            galeria.appendChild(img);

        }

        leitor.readAsDataURL(arquivos[i]);

    }

}

/* CARRINHO */

let carrinho = [];

let total = 0;

function adicionarCarrinho(nome,preco){

    carrinho.push(nome + " - R$ " + preco);

    total += preco;

    atualizarCarrinho();

    alert("Produto adicionado!");

}

function atualizarCarrinho(){

    let lista =
    document.getElementById("listaCarrinho");

    lista.innerHTML = "";

    carrinho.forEach(function(item){

        let li =
        document.createElement("li");

        li.innerText = item;

        lista.appendChild(li);

    });

    document.getElementById("total")
    .innerText = total;

}

/* PESQUISA */

function pesquisarProduto(){

    let pesquisa =
    document.getElementById("pesquisa")
    .value.toLowerCase();

    let cards =
    document.querySelectorAll(".card");

    cards.forEach(function(card){

        let nome =
        card.querySelector("h2")
        .innerText.toLowerCase();

        if(nome.includes(pesquisa)){

            card.style.display = "block";

        }else{

            card.style.display = "none";

        }

    });

}

/* FINALIZAR */

function finalizarPedido(){

    let endereco =
    document.getElementById("endereco")
    .value;

    let telefone =
    document.getElementById("telefone")
    .value;

    if(carrinho.length == 0){

        alert("Carrinho vazio!");

        return;

    }

    if(endereco == "" || telefone == ""){

        alert("Preencha endereço e telefone!");

        return;

    }

    let mensagem = "Pedido:%0A";

    carrinho.forEach(function(item){

        mensagem += "- " + item + "%0A";

    });

    mensagem +=
    "%0ATotal: R$ " + total;

    mensagem +=
    "%0AEndereço: " + endereco;

    mensagem +=
    "%0ATelefone: " + telefone;

    window.open(
        "https://wa.me/5589994033828?text="
        + mensagem,
        "_blank"
    );

}

</script>

</body>
</html>
