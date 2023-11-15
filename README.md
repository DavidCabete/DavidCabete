<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loja de Móveis</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <header>
        <h1>Loja de Móveis</h1>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Produtos</a></li>
                <li><a href="#">Contato</a></li>
            </ul>
        </nav>
    </header>

    <section id="products">
        <!-- Conteúdo dos produtos aqui -->
    </section>

    <footer>
        <p>&copy; 2023 Loja de Móveis</p>
    </footer>

    <script src="scripts.js"></script>
</body>
</html>
2. Estilização com CSS (styles.css):

css
Copy code
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: white;
    padding: 1em;
    text-align: center;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

nav li {
    display: inline;
    margin-right: 20px;
}

section {
    padding: 20px;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em;
    position: fixed;
    bottom: 0;
    width: 100%;
}
3. Adicionando Produtos com JavaScript (scripts.js):

javascript
Copy code
// Exemplo de dados de produtos
const produtos = [
    { nome: 'Sofá', preco: 500 },
    { nome: 'Cadeira', preco: 100 },
    { nome: 'Mesa de Jantar', preco: 300 },
    // Adicione mais produtos conforme necessário
];

document.addEventListener('DOMContentLoaded', function () {
    const sectionProdutos = document.getElementById('products');

    // Adiciona produtos à seção
    produtos.forEach(produto => {
        const card = document.createElement('div');
        card.classList.add('card');
        card.innerHTML = `
            <h3>${produto.nome}</h3>
            <p>Preço: $${produto.preco}</p>
            <button onclick="adicionarAoCarrinho('${produto.nome}', ${produto.preco})">Adicionar ao Carrinho</button>
        `;
        sectionProdutos.appendChild(card);
    });
});

// Função para simular adição ao carrinho (pode ser expandida conforme necessário)
function adicionarAoCarrinho(nome, preco) {
    alert(`${nome} adicionado ao carrinho por $${preco}`);
}

<!---
DavidCabete/DavidCabete is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
