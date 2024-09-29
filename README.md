HTML:

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha Loja</title>
    <link rel="stylesheet" href="site.css">
</head>
<body>
    <!-- Cabeçalho -->
    <header>
        <div class="logo">
            <h1>DWF Multistore</h1>
        </div>
        <div class="search-bar">
            <input type="text" placeholder="Buscar...">
            <button>Buscar</button>
        </div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#produtos">Produtos</a></li>
                <li><a href="carrinho.html">Carrinho</a></li>
                <li><a href="login.html">Login/Cadastro</a></li>
            </ul>
        </nav>
    </header>

    <!-- Carrossel -->
    <section class="banner" id="home">
        <div class="carousel">
            <div class="carousel-item active">
                <img src="banner.png" alt="Promoção Especial 1">
            </div>
            <div class="carousel-item">
                <img src="uno.png" alt="Promoção Especial 2">
            </div>
            <div class="carousel-item">
                <img src="deadpool.png" alt="Promoção Especial 3">
            </div>
            <button class="carousel-control prev" onclick="moveSlide(-1)">&#10094;</button>
            <button class="carousel-control next" onclick="moveSlide(1)">&#10095;</button>
        </div>
    </section>

    <!-- Produtos -->
    <section class="produtos" id="produtos">
        <h2>Destaques</h2>
        <div class="produtos-grid">
            <div class="produto-item">
                <img src="mcqueen.png" alt="Produto 1">
                <h3>Mcqueen carros</h3>
                <p>R$ 99,90</p>
                <button onclick="adicionarAoCarrinho('Mcqueen carros')">Comprar</button>
            </div>
            <div class="produto-item">
                <img src="boneca.png" alt="Produto 2">
                <h3>Boneca</h3>
                <p>R$ 79,90</p>
                <button onclick="adicionarAoCarrinho('Boneca')">Comprar</button>
            </div>
            <div class="produto-item">
                <img src="arma.png" alt="Produto 3">
                <h3>Pistola nerf</h3>
                <p>R$ 69,90</p>
                <button onclick="adicionarAoCarrinho('Pistola nerf')">Comprar</button>
            </div>
            <div class="produto-item">
                <img src="celular.png" alt="Produto 4">
                <h3>Buba celular</h3>
                <p>R$ 24,90</p>
                <button onclick="adicionarAoCarrinho('Buba celular')">Comprar</button>
            </div>
        </div>
    </section>

    <!-- Rodapé -->
    <footer>
        <p>&copy; 2024 DWF Multistore - Todos os direitos reservados.</p>
    </footer>

    <script>
        // Função para adicionar produto ao carrinho
        function adicionarAoCarrinho(produto) {
            window.location.href = `carrinho.html?produto=${produto}`;
        }

        // Lógica do Carrossel
        let currentSlide = 0;
        const slides = document.querySelectorAll('.carousel-item');
        const totalSlides = slides.length;

        function showSlide(index) {
            slides.forEach((slide, i) => {
                slide.classList.toggle('active', i === index);
            });
        }

        function moveSlide(direction) {
            currentSlide = (currentSlide + direction + totalSlides) % totalSlides;
            showSlide(currentSlide);
        }

        // Iniciar o carrossel com o primeiro slide
        showSlide(currentSlide);
    </script>
</body>
</html>









<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login/Cadastro</title>
    <link rel="stylesheet" href="login.css">
</head>
<body>
    <header>
        <div class="logo">
            <h1>DWF Multistore</h1>
        </div>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="index.html#produtos">Produtos</a></li>
                <li><a href="login.html">Login/Cadastro</a></li>
                <li><a href="carrinho.html">Carrinho</a></li>
            </ul>
        </nav>
    </header>

    <section class="login-cadastro">
        <div class="login">
            <h2>Login</h2>
            <form action="#" method="POST">
                <label for="email">E-mail:</label>
                <input type="email" id="email" name="email" required>
                
                <label for="senha">Senha:</label>
                <input type="password" id="senha" name="senha" required>
                
                <button type="submit">Entrar</button>
            </form>
        </div>

        <div class="cadastro">
            <h2>Cadastro</h2>
            <form action="#" method="POST">
                <label for="nome">Nome Completo:</label>
                <input type="text" id="nome" name="nome" required>
                
                <label for="email-cadastro">E-mail:</label>
                <input type="email" id="email-cadastro" name="email" required>
                
                <label for="senha-cadastro">Senha:</label>
                <input type="password" id="senha-cadastro" name="senha" required>
                
                <label for="confirma-senha">Confirme a Senha:</label>
                <input type="password" id="confirma-senha" name="confirma-senha" required>
                
                <button type="submit">Cadastrar</button>
            </form>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 DWF Multistore - Todos os direitos reservados.</p>
    </footer>
</body>
</html>









<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carrinho de Compras</title>
    <link rel="stylesheet" href="carrinho.css">
</head>
<body>
    <header>
        <div class="logo">
            <h1>DWF Multistore</h1>
        </div>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="index.html#produtos">Produtos</a></li>
                <li><a href="login.html">Login/Cadastro</a></li>
                <li><a href="carrinho.html">Carrinho</a></li>
            </ul>
        </nav>
    </header>

    <section class="carrinho">
        <h2>Seu Carrinho de Compras</h2>
        <div id="carrinho-container">
            <div class="carrinho-item">
                <img src="mcqueen.png" alt="Mcqueen Carros">
                <div class="carrinho-item-info">
                    <h2>Mcqueen Carros</h2>
                    <p>Preço: R$ 99,90</p>
                </div>
            </div>
            <div class="carrinho-item">
                <img src="boneca.png" alt="Boneca">
                <div class="carrinho-item-info">
                    <h2>Boneca</h2>
                    <p>Preço: R$ 79,90</p>
                </div>
            </div>
        </div>

        <div class="total-container">
            <div class="subtotal-box">
                <h3>Subtotal: R$ 179,80</h3>
            </div>
            <div class="button-container"> <!-- Adiciona um contêiner para os botões -->
                <button onclick="finalizarCompra()">Finalizar Compra</button>
                <button onclick="window.location.href='index.html#produtos'">Continuar Comprando</button>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 DWF Multistore - Todos os direitos reservados.</p>
    </footer>

    <script>
        function finalizarCompra() {
            alert("Compra finalizada com sucesso!");
        }
    </script>
</body>
</html>


CSS:

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    color: #333;
}

header {
    background-color: #df1515; /* Cor do cabeçalho */
    color: #fff; /* Cor do texto no cabeçalho */
    padding: 10px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo h1 {
    margin: 0;
    color: white; /* Nome da empresa em branco */
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

.search-bar {
    display: flex;
    align-items: center;
}

.search-bar input {
    padding: 5px;
    padding-left: 30px;
    padding-right: 60px;
    border: none;
    border-radius: 3px;
}

.search-bar button {
    padding: 5px 10px;
    margin-left: 10px;
    border: none;
    background-color: #af0606; /* Botão de busca */
    color: #fff;
    cursor: pointer;
    border-radius: 3px;
}

nav ul {
    list-style: none;
    display: flex;
    gap: 15px;
}

nav ul li {
    display: inline;
    position: relative; /* Para o uso do pseudo-elemento */
}

nav ul li a {
    color: #fff; /* Cor do texto visível inicialmente */
    text-decoration: none; /* Remove o sublinhado padrão */
    padding: 5px 0; /* Espaçamento vertical para a linha */
    transition: color 0.3s; /* Animação suave para a cor do texto */
    position: relative; /* Para o uso do pseudo-elemento para a linha */
}

nav ul li a::after {
    content: '';
    display: block;
    height: 2px; /* Altura da linha */
    background-color: #fff; /* Cor da linha */
    width: 100%; /* Largura da linha */
    position: absolute; /* Posição absoluta em relação ao link */
    left: 0; /* Alinha à esquerda */
    top: 100%; /* Coloca a linha logo abaixo do texto */
    transform: scaleX(0); /* Inicialmente, a linha não é visível */
    transition: transform 0.3s; /* Animação suave para a largura da linha */
}

nav ul li a:hover::after {
    transform: scaleX(1); /* A linha se expande ao passar o mouse */
}

nav ul li a:hover {
    color: #fff; /* A cor do texto permanece a mesma ao passar o mouse */
}

/* Estilo para a linha intuitiva */
nav ul li a::before {
    content: ''; /* Adiciona a linha intuitiva */
    display: block;
    height: 2px; /* Altura da linha */
    background-color: #fff; /* Cor da linha */
    width: 100%; /* Largura da linha */
    position: absolute; /* Posição absoluta em relação ao link */
    left: 0; /* Alinha à esquerda */
    bottom: 0; /* Coloca a linha logo abaixo do texto */
    z-index: -1; /* Coloca a linha atrás do texto */
    transition: transform 0.3s; /* Animação suave para a largura da linha */
}

nav ul li:hover a {
    color: #fff; /* A cor do texto permanece a mesma ao passar o mouse */
}

nav ul li a:hover::before {
    transform: scaleX(1); /* A linha se expande ao passar o mouse */
}

.banner {
    text-align: center;
    margin: 20px 0;
}

.banner img {
    max-width: 100%;
    height: auto;
}

/* Estilo para o carrossel */
.carousel {
    position: relative;
    max-width: 100%;
    overflow: hidden;
}

.carousel-item {
    display: none; /* Inicialmente escondido */
    text-align: center;
    opacity: 0; /* Iniciar com opacidade 0 para a animação */
    transition: opacity 0.5s ease-in-out, transform 0.5s ease; /* Animação suave */
}

.carousel-item.active {
    display: block; /* Exibe apenas o item ativo */
    opacity: 1; /* Define a opacidade para 1 do item ativo */
    transform: translateX(0); /* Mantém a posição original do item ativo */
}

.carousel-item:not(.active) {
    transform: translateX(100%); /* Move os itens não ativos para fora à direita */
}

/* Estilo das imagens do carrossel */
.carousel-item img {
    width: 100%;
    height: 100%; /* Define a altura para preencher o contêiner */
    object-fit: contain; /* Mantém a proporção da imagem, mas ajusta ao contêiner */
    max-height: 400px; /* Define uma altura máxima para o carrossel */
}

/* Botões de controle do carrossel */
.carousel-control {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    z-index: 10;
    border-radius: 50%; /* Botões redondos */
    transition: background-color 0.3s; /* Animação para a cor de fundo */
}

.carousel-control:hover {
    background-color: rgba(0, 0, 0, 0.8); /* Cor do botão ao passar o mouse */
}

.carousel-control.prev {
    left: 10px;
}

.carousel-control.next {
    right: 10px;
}

/* Estilo para a seção de produtos */
.produtos {
    padding: 20px;
    background-color: #fff;
    margin-bottom: 20px;
}

.produtos h2 {
    margin-bottom: 20px;
    color: #ff0000; /* Título "Destaques" em vermelho chamativo */
}

.produtos-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
}

.produto-item {
    background-color: #f9f9f9;
    padding: 15px;
    text-align: center;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.produto-item img {
    width: 100%;
    height: 150px;
    object-fit: contain; /* Mantém a proporção da imagem */
    margin-bottom: 10px;
}

.produto-item h3 {
    font-size: 1.2em;
    margin-bottom: 10px;
    color: #007bff; /* Cor chamativa para os nomes dos brinquedos (azul padrão) */
}

.produto-item p {
    color: #e70c0c; /* Preço em vermelho */
    font-weight: bold;
    margin-bottom: 15px;
}

.produto-item button {
    padding: 10px;
    background-color: #b80808; /* Cor do botão "Comprar" */
    color: #fff;
    border: none;
    cursor: pointer;
    border-radius: 3px;
}

.produto-item button:hover {
    background-color: #eb0f0f; /* Cor do botão ao passar o mouse */
}

/* Estilo do carrinho */
.carrinho {
    padding: 20px;
    background-color: #fff;
    margin-bottom: 20px;
}

.carrinho h2 {
    margin-bottom: 20px;
}

.carrinho-item {
    background-color: #f9f9f9;
    padding: 15px;
    border: 1px solid #ddd;
    border-radius: 5px;
    margin-bottom: 10px;
}

/* Estilo para login e cadastro */
.login-cadastro {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    padding: 20px;
    background-color: #fff;
}

.login, .cadastro {
    flex: 1;
    background-color: #f9f9f9;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.login h2, .cadastro h2 {
    margin-bottom: 15px;
}

.login form, .cadastro form {
    display: flex;
    flex-direction: column;
}

.login form label, .cadastro form label {
    margin-bottom: 5px;
}

.login form input, .cadastro form input {
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #ddd;
}

/* Botão de login e cadastro */
.login form button, .cadastro form button {
    padding: 10px;
    background-color: #df1515; /* Cor do botão em login e cadastro */
    color: #fff;
    border: none;
    cursor: pointer;
    border-radius: 3px;
}

.login form button:hover, .cadastro form button:hover {
    background-color: #af0606; /* Cor do botão ao passar o mouse */
}

/* Responsividade */
@media (max-width: 768px) {
    .login, .cadastro {
        width: 100%;
    }
}









/* Layout básico */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f8f9fa;
}

header {
    background-color: #df1515;
    color: white;
    padding: 15px;
    display: flex;
    justify-content: space-between; /* Para distribuir logo e nav */
    align-items: center; /* Para centralizar verticalmente */
}

header .logo h1 {
    margin: 0;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

header nav {
    margin-left: auto; /* Para empurrar o nav para a direita */
}

header nav ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex;
}

header nav ul li {
    margin-left: 20px; /* Espaçamento entre os itens do menu */
}

header nav ul li a {
    color: white;
    text-decoration: none;
}

header nav ul li a:hover {
    text-decoration: underline;
}

.search-bar {
    margin-top: 10px;
}

.search-bar input {
    padding: 10px;
    width: 250px;
    margin-right: 5px;
}

.search-bar button {
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    border: none;
    cursor: pointer;
}

.search-bar button:hover {
    background-color: #0056b3;
}

/* Banner */
.banner img {
    width: 100%;
    height: auto;
}

/* Produtos */
.produtos {
    padding: 40px;
}

.produtos-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

.produto-item {
    width: 23%;
    margin-bottom: 20px;
    text-align: center;
    padding: 20px;
    background-color: white;
    border: 1px solid #ddd;
    border-radius: 10px;
    transition: box-shadow 0.3s;
}

.produto-item:hover {
    box-shadow: 0 4px 8px rgba(250, 0, 0, 0.1);
}

.produto-item img {
    width: 100%;
    height: 150px;
    object-fit: contain;
    margin-bottom: 15px;
}

.produto-item h3 {
    font-size: 18px;
    margin-bottom: 10px;
}

.produto-item p {
    font-size: 16px;
    color: #28a745;
}

.produto-item button {
    padding: 10px 20px;
    background-color: #28a745;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.produto-item button:hover {
    background-color: #218838;
}

/* Login/Cadastro */
.login-cadastro {
    display: flex;
    justify-content: center;
    margin: 40px 0;
}

.login, .cadastro {
    background-color: white;
    padding: 30px;
    margin: 20px;
    width: 35%;
    border: 1px solid #ddd;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.login h2, .cadastro h2 {
    margin-bottom: 20px;
    font-size: 24px;
    color: #343a40;
    text-align: center;
}

form {
    display: flex;
    flex-direction: column;
}

form label {
    margin-bottom: 5px;
    font-weight: bold;
    color: #403434;
}

form input {
    padding: 10px;
    margin-bottom: 20px;
    border: 1px solid #ddd;
    border-radius: 5px;
    font-size: 16px;
    width: 100%;
}

form button {
    padding: 12px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
}

form button:hover {
    background-color: #0056b3;
}

/* Rodapé */
footer {
    text-align: center;
    background-color: #343a40;
    color: white;
    padding: 10px;
    position: absolute;
    width: 100%;
    bottom: 0;
}

@media (max-width: 768px) {
    .login, .cadastro {
        width: 80%;
    }
}

@media (max-width: 480px) {
    .login, .cadastro {
        width: 100%;
    }

    header nav ul {
        flex-direction: column;
    }
}









/* Reset básico */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4; /* Cor de fundo */
    color: #333; /* Cor do texto */
    display: flex;
    flex-direction: column;
    min-height: 100vh; /* Garante que o corpo ocupe toda a altura da tela */
}

/* Estilo do cabeçalho */
header {
    background-color: #df1515; /* Cor de fundo do cabeçalho */
    color: #fff; /* Cor do texto */
    padding: 10px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo h1 {
    margin: 0;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

nav ul {
    list-style: none; /* Remove marcadores */
    display: flex; /* Exibe os itens em linha */
    gap: 15px; /* Espaçamento entre os itens */
}

nav ul li {
    display: inline;
}

nav ul li a {
    color: #fff; /* Cor do link */
    text-decoration: none; /* Remove o sublinhado */
}

/* Estilo da seção do carrinho */
.carrinho {
    padding: 20px;
    background-color: #fff; /* Fundo branco */
    margin: 20px; /* Margem em volta da seção */
    border-radius: 10px; /* Bordas arredondadas */
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1); /* Sombra para destaque */
    flex-grow: 1; /* Faz a seção ocupar o espaço disponível */
}

.carrinho h2 {
    margin-bottom: 20px;
    font-size: 1.8em; /* Tamanho maior para o título */
    color: #df1515; /* Cor do título */
}

/* Itens do carrinho */
.carrinho-item {
    display: flex; /* Alinha itens em linha */
    align-items: center; /* Centraliza verticalmente */
    background-color: #f9f9f9; /* Fundo dos itens do carrinho */
    padding: 15px;
    border: 1px solid #ddd; /* Borda dos itens */
    border-radius: 5px; /* Bordas arredondadas */
    margin-bottom: 15px; /* Espaçamento entre itens */
}

.carrinho-item img {
    width: 100px; /* Largura fixa para a imagem */
    height: auto; /* Altura automática para manter proporção */
    margin-right: 15px; /* Espaçamento à direita da imagem */
}

.carrinho-item-info {
    flex: 1; /* Permite que a informação do item ocupe o espaço restante */
}

.carrinho-item-info h2 {
    margin: 0; /* Remove margem do título */
    color: #007bff; /* Cor do nome do produto */
}

.carrinho-item-info p {
    margin: 5px 0; /* Margem entre parágrafos */
    color: #e70c0c; /* Preço em vermelho */
    font-weight: bold; /* Negrito */
}

/* Estilo da caixa do subtotal */
.subtotal-box {
    padding: 10px 15px; /* Espaçamento interno */
    background-color: #eaeaea; /* Cor de fundo da caixa */
    border: 1px solid #ccc; /* Borda da caixa */
    border-radius: 5px; /* Bordas arredondadas */
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); /* Sombra para destaque */
}

/* Total */
.total-container {
    display: flex;
    flex-direction: column; /* Coloca os elementos em coluna */
    align-items: flex-end; /* Alinha os itens à direita */
    margin-top: 20px; /* Espaço acima da seção total */
}

/* Títulos do subtotal */
.total-container h3 {
    font-size: 1.5em; /* Tamanho da fonte para o subtotal */
    color: #df1515; /* Cor do subtotal */
}

/* Botões */
.button-container {
    display: flex; 
    flex-direction: column; /* Coloca os botões em coluna */
    gap: 10px; /* Espaçamento entre os botões */
    margin-top: 15px; /* Espaço acima dos botões */
}

button {
    padding: 10px 15px;
    background-color: #df1515; /* Cor do botão */
    color: #fff; /* Cor do texto */
    border: none;
    cursor: pointer;
    border-radius: 5px; /* Bordas arredondadas */
    font-weight: bold; /* Negrito */
    transition: background-color 0.3s, transform 0.2s; /* Efeito de transição */
}

button:hover {
    background-color: #af0606; /* Cor ao passar o mouse */
    transform: scale(1.05); /* Leve aumento ao passar o mouse */
}

/* Estilo do rodapé */
footer {
    text-align: center;
    padding: 20px;
    background-color: #343a40; /* Cor de fundo do rodapé */
    color: #fff; /* Cor do texto */
    position: relative; /* Posicionamento do rodapé */
    bottom: 0; /* Fixa na parte inferior */
    width: 100%; /* Largura total */
}

/* Responsividade */
@media (max-width: 768px) {
    .carrinho {
        margin: 10px; /* Reduzir margem em telas menores */
    }

    .carrinho-item {
        flex-direction: column; /* Coloca a imagem acima do texto em telas menores */
        align-items: flex-start; /* Alinha itens à esquerda */
    }

    .carrinho-item img {
        margin-bottom: 10px; /* Espaço abaixo da imagem */
    }
}
