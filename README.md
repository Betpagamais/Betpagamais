<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BetPagaMais - Apostas Esportivas</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>BetPagaMais</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#apostas">Apostas</a></li>
                <li><a href="#conta">Minha Conta</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="home">
            <h2>Bem-vindo à BetPagaMais</h2>
            <p>A melhor plataforma de apostas esportivas do Brasil! Aposte agora e ganhe prêmios incríveis.</p>
        </section>

        <section id="apostas">
            <h2>Apostas ao Vivo</h2>
            <div class="evento">
                <h3>Futebol - Flamengo vs Palmeiras</h3>
                <p>Escolha seu time favorito para vencer:</p>
                <button onclick="apostar('Flamengo')">Flamengo</button>
                <button onclick="apostar('Palmeiras')">Palmeiras</button>
                <button onclick="apostar('Empate')">Empate</button>
            </div>
        </section>

        <section id="conta">
            <h2>Minha Conta</h2>
            <p>Saldo: <span id="saldo">R$100,00</span></p>
            <p>Histórico de Apostas: <span id="historico"></span></p>
        </section>

        <section id="contato">
            <h2>Fale Conosco</h2>
            <form id="contatoForm">
                <label for="nome">Nome:</label>
                <input type="text" id="nome" name="nome" required>
                <label for="mensagem">Mensagem:</label>
                <textarea id="mensagem" name="mensagem" required></textarea>
                <button type="submit">Enviar</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 BetPagaMais. Todos os direitos reservados.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>- 
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
}

header h1 {
    margin: 0;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

main {
    padding: 20px;
}

section {
    margin-bottom: 40px;
}

h2 {
    color: #333;
}

button {
    padding: 10px 20px;
    margin: 10px;
    background-color: #333;
    color: #fff;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #555;
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}
let saldo = 100;
let historico = [];

function apostar(time) {
    const valorAposta = 10; // Valor fixo para cada aposta
    if (saldo >= valorAposta) {
        saldo -= valorAposta;
        historico.push(`Você apostou no ${time}`);
        atualizarInterface();
        alert(`Aposta feita no ${time}! Boa sorte!`);
    } else {
        alert('Saldo insuficiente para apostar.');
    }
}

function atualizarInterface() {
    document.getElementById('saldo').textContent = `R$${saldo.toFixed(2)}`;
    document.getElementById('historico').textContent = historico.join(', ');
}

document.getElementById('contatoForm').addEventListener('submit', function(event) {
    event.preventDefault();
    alert('Mensagem enviada com sucesso!');
});
👋 Hi, I’m @Betpagamais
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Betpagamais/Betpagamais is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
