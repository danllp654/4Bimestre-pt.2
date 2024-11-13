<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsividade com HTML e CSS - Alura</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#">Início</a></li>
                <li><a href="#">Sobre</a></li>
                <li><a href="#">Serviços</a></li>
                <li><a href="#">Contato</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="intro">
            <h1>Bem-vindo à nossa página responsiva!</h1>
            <p>Aprendendo a criar layouts flexíveis e responsivos com HTML e CSS.</p>
        </section>

        <section class="content">
            <article>
                <h2>O que é Responsividade?</h2>
                <p>A responsividade é uma técnica que permite que o design de um site se ajuste automaticamente ao tamanho da tela do dispositivo do usuário.</p>
            </article>

            <article>
                <h2>Como Funciona?</h2>
                <p>Utilizamos Media Queries, Flexbox e Grid Layouts para criar designs que se adaptam a diferentes dispositivos, como celulares, tablets e desktops.</p>
            </article>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Responsividade em Aplicações - Alura</p>
    </footer>
</body>
</html>

/* Reset básico */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Corpo e fontes */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #f4f4f4;
}

/* Cabeçalho e Navegação */
header {
    background-color: #333;
    color: white;
    padding: 1rem 0;
}

nav ul {
    list-style-type: none;
    display: flex;
    justify-content: center;
}

nav ul li {
    margin: 0 15px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

nav ul li a:hover {
    text-decoration: underline;
}

/* Seção de conteúdo principal */
main {
    padding: 20px;
    max-width: 1200px;
    margin: 0 auto;
}

.intro {
    text-align: center;
    margin-bottom: 30px;
}

.intro h1 {
    font-size: 2.5rem;
    color: #333;
}

.intro p {
    font-size: 1.2rem;
    color: #555;
}

/* Layout de conteúdo */
.content {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    flex-wrap: wrap;
}

.content article {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    width: 48%;
}

.content article h2 {
    font-size: 1.5rem;
    margin-bottom: 10px;
}

.content article p {
    font-size: 1rem;
    color: #555;
}

/* Rodapé */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
    margin-top: 50px;
}

/* Media Queries - Responsividade */
@media (max-width: 768px) {
    .content {
        flex-direction: column;
        align-items: center;
    }

    .content article {
        width: 80%;
        margin-bottom: 20px;
    }

    .intro h1 {
        font-size: 2rem;
    }

    .intro p {
        font-size: 1rem;
    }
}

@media (max-width: 480px) {
    nav ul {
        flex-direction: column;
    }

    nav ul li {
        margin: 10px 0;
    }

    .intro h1 {
        font-size: 1.8rem;
    }

    .intro p {
        font-size: 1rem;
    }

    .content article {
        width: 100%;
    }
}

