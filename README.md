Como Criar um Card Digital com Modal Usando Bootstrap e jQuery

Bem-vindo(a) ao meu tutorial! Aqui, você vai aprender, passo a passo, como criar um card digital com uma foto e um modal que exibe mais informações ao clicar em um botão. Vamos usar Bootstrap para o estilo e jQuery para a interatividade. Este é um projeto simples e ótimo para iniciantes em desenvolvimento web!
Pré-requisitos

    Um editor de código (como VS Code).
    Conexão com a internet (para carregar os CDNs do Bootstrap e jQuery).
    Uma imagem para usar no card (opcional).

Resultado Final

Ao final, você terá um card com:

    Uma foto no topo.
    Um título e descrição.
    Um botão que abre um modal com mais detalhes.

Vamos começar!
Passo a Passo
Passo 1: Criar a Estrutura Básica do HTML

Primeiro, criamos um arquivo HTML básico e adicionamos as dependências do Bootstrap e jQuery.

    Crie um arquivo chamado index.html.
    Adicione este código:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Card Digital</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Nosso CSS personalizado -->
    <style>
        .card-img-top {
            height: 200px;
            object-fit: cover;
        }
    </style>
</head>
<body>
    <!-- Conteúdo será adicionado aqui -->

    <!-- Scripts -->
    <script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>

O que fizemos:

    Definimos o documento como HTML5 com <!DOCTYPE html>.
    Adicionamos suporte a caracteres especiais com <meta charset="UTF-8">.
    Tornamos o layout responsivo com <meta name="viewport">.
    Incluímos o CSS do Bootstrap via CDN.
    Adicionamos um <style> para ajustar a altura da imagem do card.
    Carregamos o jQuery e o JS do Bootstrap no final do <body>.

Passo 2: Adicionar o Card

Vamos criar o card dentro de um container para organizar o layout.

    Dentro do <body>, antes dos scripts, adicione:

<!-- Container para centralizar o conteúdo -->
<div class="container mt-5">
    <!-- Linha do grid -->
    <div class="row">
        <!-- Coluna ocupando 4 de 12 unidades (33% da largura em telas médias) -->
        <div class="col-md-4">
            <!-- Estrutura do card -->
            <div class="card">
                <img class="card-img-top" src="img/perfil.jpg" alt="Foto de perfil">
                <div class="card-body">
                    <h5 class="card-title">Hi! My name is Gustavo!</h5>
                    <p class="card-text">I'm a front-end developer.</p>
                    <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
                        About more
                    </button>
                </div>
            </div>
        </div>
    </div>
</div>

O que fizemos:

    Usamos .container para centralizar o conteúdo e .mt-5 para adicionar margem superior.
    Criamos uma .row e uma .col-md-4 para o card ocupar 33% da largura em telas médias.
    Dentro do .card, adicionamos:
        Uma imagem com .card-img-top.
        Um .card-body com título, texto e um botão.
    O botão tem data-bs-toggle="modal" e data-bs-target="#exampleModal" para abrir o modal (que criaremos no próximo passo).

Nota: Substitua img/perfil.jpg pelo caminho da sua imagem ou use uma URL como https://via.placeholder.com/300x200.
Passo 3: Criar o Modal

Agora, vamos adicionar o modal que aparece ao clicar no botão.

    Após o </div> do container, adicione:

<!-- Modal -->
<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog">
        <div class="modal-content">
            <!-- Cabeçalho do modal -->
            <div class="modal-header">
                <h5 class="modal-title" id="exampleModalLabel">About me</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <!-- Corpo do modal -->
            <div class="modal-body">
                <img class="img-fluid mb-3" src="img/perfil.jpg" alt="Foto de perfil">
                <p>I'm Gustavo, a passionate front-end developer with experience in HTML, CSS, JavaScript, and frameworks like Bootstrap.</p>
            </div>
            <!-- Rodapé do modal -->
            <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
            </div>
        </div>
    </div>
</div>

O que fizemos:

    Criamos um .modal com o ID exampleModal (o mesmo do data-bs-target do botão).
    Usamos .modal-dialog e .modal-content para estruturar o modal.
    Dividimos em:
        .modal-header: título e botão de fechar.
        .modal-body: imagem responsiva (.img-fluid) e texto.
        .modal-footer: botão para fechar.
    O atributo data-bs-dismiss="modal" fecha o modal ao clicar no botão.

Passo 4: Testar o Projeto

    Salve o arquivo index.html.
    Abra em um navegador.
    Clique no botão "About more" para ver o modal abrir.

Dica: Se a imagem não carregar, verifique o caminho em src="img/perfil.jpg" ou use uma URL online.
Código Completo

Aqui está o código final para referência:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Card Digital</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        .card-img-top {
            height: 200px;
            object-fit: cover;
        }
    </style>
</head>
<body>
    <div class="container mt-5">
        <div class="row">
            <div class="col-md-4">
                <div class="card">
                    <img class="card-img-top" src="img/perfil.jpg" alt="Foto de perfil">
                    <div class="card-body">
                        <h5 class="card-title">Hi! My name is Gustavo!</h5>
                        <p class="card-text">I'm a front-end developer.</p>
                        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
                            About more
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="exampleModalLabel">About me</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <img class="img-fluid mb-3" src="img/perfil.jpg" alt="Foto de perfil">
                    <p>I'm Gustavo, a passionate front-end developer with experience in HTML, CSS, JavaScript, and frameworks like Bootstrap.</p>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                </div>
            </div>
        </div>
    </div>
    <script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>

Personalização

    Imagem: Substitua img/perfil.jpg por sua própria foto.
    Texto: Edite o título, descrição e conteúdo do modal com suas informações.
    Estilo: Modifique o CSS no <style> para mudar cores, tamanhos ou adicionar efeitos.

Conclusão

Parabéns! Você criou um card digital interativo com Bootstrap e jQuery. Este é um ótimo exemplo para portfólios ou para ensinar HTML, CSS e JavaScript. Se precisar de mais ideias ou ajustes, deixe um comentário no repositório!

Feito por [Gustavo Henrique] - [https://www.linkedin.com/in/henri-mattos/].