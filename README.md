# Post Comment React App

Este repositório contém um aplicativo React simples de comentário de post.

### Pré-requisitos

Certifique-se de ter o Node.js instalado em seu sistema antes de executar este aplicativo.

- Node.js: [Baixe aqui](https://nodejs.org)

### Instalação

1. Clone o repositório para o seu diretório local:

```shell
git clone <URL do repositório>
```

2. Navegue até o diretório do projeto:

```shell
cd <nome do diretório>
```

3. Instale as dependências necessárias:

```shell
npm install
```

### Executando o Aplicativo

Depois de concluir a instalação, você pode iniciar o aplicativo executando o seguinte comando:

```shell
npm run dev
```

Isso iniciará o aplicativo React em modo de desenvolvimento. Abra o navegador e acesse `http://localhost:5173` para visualizar o aplicativo.

Qualquer alteração no código-fonte será automaticamente recarregada no navegador.

### Construção do Projeto

Para criar uma versão otimizada do aplicativo para produção, execute o seguinte comando:

```shell
npm run build
```

Isso criará uma pasta `build` no diretório do projeto com os arquivos otimizados para produção.

--------------------------------------
Funcionalidades Testadas:

1. Acesso à Aplicação

- Visita a URL local da aplicação (http://localhost:5173/)

2. Inserção de Comentário

- Localiza a caixa de comentários usando o seletor [data-qa="comment-input"]

- Digita o texto "Teste 123" no primeiro campo de comentário encontrado

- Aciona o botão de publicação usando [data-qa=publish-button]

3. Validação de Publicação

- Verifica se o comentário foi criado com sucesso buscando pelo texto "Teste 123"

4. Limpeza de Dados (Exclusão do Comentário)

- Percorre todos os comentários existentes na página

- Localiza o comentário de teste através do texto

- Aciona o botão de exclusão correspondente ao comentário

- Usa a relação entre elementos irmãos para encontrar o botão de delete

Estrutura do Teste:
- Framework: Cypress
- Padrão de Seletores: Atributos data-qa para melhor identificação de elementos
- Comportamento: Teste end-to-end (e2e) que simula ações reais do usuário

Como Executar:
1. Certifique-se que a aplicação está rodando em http://localhost:5173/
2. Execute o comando de testes Cypress:
```bash
npx cypress run
```
Observações:
- O teste inclui limpeza automática dos dados criados durante a execução
- Usa seletores dedicados (data-qa) para maior resiliência às mudanças na UI
- Verifica tanto a criação quanto a exclusão para manter o estado inicial da aplicação

Este teste assegura que a funcionalidade de comentários mantém seu comportamento esperado após novas implementações ou modificações no código.

