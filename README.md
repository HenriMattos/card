# Como Criar um Card Digital com Modal Usando Bootstrap e jQuery

Bem-vindo(a) ao meu tutorial! Aqui, você vai aprender, passo a passo, como criar um card digital com uma foto e um modal que exibe mais informações ao clicar em um botão. Vamos usar Bootstrap para o estilo e jQuery para a interatividade. Este é um projeto simples e ótimo para iniciantes em desenvolvimento web!

## Pré-requisitos

- Um editor de código (como VS Code).
- Conexão com a internet (para carregar os CDNs do Bootstrap e jQuery).
- Uma imagem para usar no card (opcional).

## Resultado Final

Ao final, você terá um card com:

- Uma foto no topo.
- Um título e descrição.
- Um botão que abre um modal com mais detalhes.

Vamos começar!

---

## Passo a Passo

### Passo 1: Criar a Estrutura Básica do HTML

Primeiro, criamos um arquivo HTML básico e adicionamos as dependências do Bootstrap e jQuery.

1. Crie um arquivo chamado `index.html`.
2. Adicione a estrutura básica do HTML, incluindo as referências ao Bootstrap e jQuery.
3. Inclua um bloco de estilo para ajustar a altura da imagem do card.

O que foi feito:

- Definição do documento como HTML5.
- Suporte a caracteres especiais e design responsivo.
- Inclusão do CSS do Bootstrap via CDN.
- Adição do jQuery e do JS do Bootstrap no final do `body`.

### Passo 2: Adicionar o Card

Agora, vamos criar o card dentro de um container para organizar o layout.

1. Adicione um `container` para centralizar o conteúdo.
2. Dentro do `container`, crie uma `row` e uma `col-md-4` para definir a largura do card.
3. Insira a estrutura do card, contendo:
   - Uma imagem no topo.
   - Um título e uma descrição.
   - Um botão que abrirá o modal.

Dicas:

- O botão precisa conter os atributos `data-bs-toggle="modal"` e `data-bs-target="#exampleModal"` para abrir o modal.
- Substitua `img/perfil.jpg` pelo caminho da sua imagem ou use uma URL, como `https://via.placeholder.com/300x200`.

### Passo 3: Criar o Modal

Agora, vamos adicionar o modal que aparece ao clicar no botão.

1. Adicione um modal com um ID correspondente ao `data-bs-target` do botão.
2. Estruture o modal em três partes:
   - **Cabeçalho:** Título e botão de fechar.
   - **Corpo:** Imagem e texto descritivo.
   - **Rodapé:** Botão para fechar o modal.

O que foi feito:

- Definição de um modal com `.modal-dialog` e `.modal-content`.
- Inclusão de um botão de fechar com `data-bs-dismiss="modal"`.

### Passo 4: Testar o Projeto

1. Salve o arquivo `index.html`.
2. Abra-o em um navegador.
3. Clique no botão "About more" para verificar se o modal abre corretamente.

Dica: Se a imagem não carregar, verifique o caminho especificado ou utilize uma URL online.

---

## Personalização

- **Imagem:** Substitua `img/perfil.jpg` por sua própria foto.
- **Texto:** Edite o título, descrição e conteúdo do modal com suas informações.
- **Estilo:** Modifique o CSS para mudar cores, tamanhos ou adicionar efeitos personalizados.

## Conclusão

Parabéns! Você criou um card digital interativo com Bootstrap e jQuery. Este é um ótimo exemplo para portfólios ou para ensinar HTML, CSS e JavaScript. Se precisar de mais ideias ou ajustes, deixe um comentário no repositório!

---

**Feito por [Gustavo Henrique](https://www.linkedin.com/in/henri-mattos/).**