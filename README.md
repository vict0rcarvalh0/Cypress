# Cypress
## O que é Cypress e para que serve?
Cypress é uma ferramenta de automação de testes end-to-end (E2E) para aplicativos da web modernos. É construído em Node.js e oferecido como um módulo npm, apesar de sua construção em Node, a maioria das funcionalidades são executadas por comandos. Ele é usado principalmente por desenvolvedores e equipes de teste para testar a funcionalidade de ponta a ponta de seus aplicativos da web de forma automatizada.

## Vantagens e desvantagens do Cypress em relação a outras ferramentas
<img width="80%" src="https://www.toolsqa.com/gallery/Cypress/6.Selenium%20vs%20Cypress.png">

### 1. Velocidade (Speed):

- Cypress: O Cypress é conhecido por sua velocidade superior de execução de testes, devido ao seu modelo de arquitetura e à maneira como interage com o navegador.
- Selenium: O Selenium pode ser mais lento em comparação com o Cypress, especialmente em cenários complexos, devido à sua abordagem baseada em WebDriver.

### 2. Espera por Elemento (Wait for Element):

- Cypress: O Cypress tem uma espera automática embutida, o que significa que não é necessário explicitamente adicionar comandos de espera para aguardar que os elementos apareçam na página.
- Selenium: No Selenium, é necessário adicionar comandos explícitos de espera para aguardar que os elementos sejam carregados na página.

### 3. Execução Remota (Remote Execution):

- Cypress: O Cypress é mais adequado para execução local de testes e não possui suporte nativo para execução remota.
- Selenium: O Selenium é mais flexível em termos de execução remota, pois pode ser configurado para executar testes em ambientes remotos usando ferramentas como Selenium Grid ou serviços de nuvem.

### 4. Execução Paralela (Parallel Execution):

- Cypress: O Cypress oferece suporte limitado para execução paralela, principalmente por meio de ferramentas de terceiros ou serviços de integração contínua.
- Selenium: O Selenium oferece suporte nativo para execução paralela por meio do Selenium Grid ou serviços de nuvem.

### 5. Modo Headless:

- Cypress: O Cypress oferece suporte nativo para execução em modo headless, o que pode ser útil para execução de testes em servidores de integração contínua ou ambientes de CI/CD.
- Selenium: O Selenium também oferece suporte para execução em modo headless, embora às vezes possa ser menos estável do que o modo com navegador visível.

### 6. Captura de Tela (Screenshot):

- Cypress: O Cypress oferece recursos embutidos para captura de tela, permitindo que os desenvolvedores capturem screenshots durante a execução dos testes.
- Selenium: O Selenium também oferece suporte para captura de tela, mas pode exigir bibliotecas externas para implementar essa funcionalidade.

### 7. Vídeo:

- Cypress: O Cypress oferece suporte nativo para gravação de vídeo durante a execução dos testes.
- Selenium: O Selenium pode gravar vídeo usando bibliotecas externas, mas não oferece suporte nativo para essa funcionalidade.

### 8. Documentação e Comunidade (Documentation, Community):

- Cypress: O Cypress possui uma documentação detalhada e uma comunidade ativa, com muitos recursos disponíveis para ajudar os desenvolvedores.
- Selenium: O Selenium também tem uma documentação abrangente e uma comunidade grande e ativa, com muitos recursos disponíveis online.

### 9. Executar JavaScript (Execute JS):

- Cypress: O Cypress permite a execução de JavaScript diretamente no contexto do aplicativo sendo testado.
- Selenium: O Selenium também oferece suporte para execução de JavaScript, mas às vezes pode ser mais complicado de implementar.

### 10. Alternar Abas (Switch Tabs):

- Cypress: O Cypress possui funcionalidade embutida para alternar entre abas do navegador durante a execução dos testes.
- Selenium: No Selenium, alternar entre abas pode ser mais complicado e requer o uso de manipulação de janelas do navegador.

### 11. Vários Navegadores (Several Browsers):

- Cypress: O Cypress atualmente suporta apenas o navegador Chrome para execução de testes.
- Selenium: O Selenium oferece suporte para vários navegadores, incluindo Chrome, Firefox, Safari, Edge e outros, através do WebDriver.

### 12. Carregar Extensões (Load Extensions):

- Cypress: O Cypress não suporta nativamente o carregamento de extensões do navegador durante a execução dos testes.
- Selenium: O Selenium pode carregar extensões do navegador como parte da configuração do WebDriver.

### 13. Gerenciar Cookies (Manage Cookies):

- Cypress: O Cypress oferece recursos para gerenciar cookies durante a execução dos testes.
- Selenium: O Selenium também oferece suporte para gerenciamento de cookies, permitindo adicionar, remover ou modificar cookies durante a execução dos testes.

## Arquitetura do Cypress
A maioria das ferramentas de teste opera fora do navegador e executa comandos remotos pela rede. Mas o mecanismo Cypress opera diretamente dentro do navegador, ou seja, o código de teste é executado pelo navegador.

Essa arquitetura permite que o Cypress ouça e modifique o comportamento do navegador em tempo de execução, manipulando o DOM(Document Object Model) e alterando solicitações e respostas da rede em tempo real. Isso permite controle total(end-to-end) sobre a aplicação e execução de testes unitários, funcionais, de integração e de ponta a ponta.

Além do DOM, o Cypress acessa ferramentas de desenvolvimento, armazenamento local, camada de rede e objetos de janela, e sem fazer uso do WebDriver.

<p align="center">
  <img src="https://user-images.githubusercontent.com/17179877/74605728-8e547a80-50c2-11ea-8549-b804ef9b4996.png" width="80%">
</p>


## Seletores de elementos no Cypress
Seletores no Cypress são métodos usados para identificar e selecionar elementos específicos em uma página da web durante a execução de testes automatizados. Eles servem como uma maneira de direcionar elementos HTML específicos para interagir com eles ou verificar seu estado durante a execução dos testes.

### `cy.contains('Text')`
Utilizado para localizar elementos que contêm um texto específico, ou seja, um conteúdo visível.

### `cy.get('#elementID' ou '.elementClass' ou 'element')`
Utilizado para selecionar elementos com base em uma variedade de critérios, como classes, IDs, atributos, texto e outros atributos

### `cy.find('.child')`
Utilizado para encontrar elementos filhos de um elemento selecionado anteriormente, é útil para selecionar elementos dentro de um contexto específico.

### `cy.eq(value)`
Utilizado para selecionar um elemento com base em seu índice dentro de um conjunto de elementos correspondentes, permite selecionar um elemento específico em uma lista de elementos.

### `cy.xpath('/path')`
Pode ser usado para seleções mais complexas baseadas em expressões XPath, isso permite uma maior flexibilidade na seleção de elementos.

## Comandos e asserções no Cypress
No contexto do Cypress, comandos e asserções são duas categorias principais de ações que você pode executar em seus testes automatizados para interagir com a aplicação sendo testada e verificar o comportamento esperado.

### Comandos

Usados para interagir com elementos da página da web, como clicar em botões, preencher campos de formulário, navegar entre páginas, etc.

**`cy.click()`**

Usado para simular um clique em um elemento na página da web durante a execução dos testes automatizados.

**`cy.visit()`**

Utilizado para navegar para uma URL específica durante a execução dos testes automatizados.

**`cy.type()`**

Usado para inserir texto em um elemento de entrada (como um campo de texto) na página da web durante a execução dos testes.

### Asserções

Usadas para verificar o estado ou o comportamento da aplicação durante a execução dos testes, podendo ser uma verificação se elementos estão visíveis, se contêm um determinado texto, se têm uma determinada classe, etc.

**`cy.should('be.visible')`**

Usada para verificar se um elemento na página está visível durante a execução dos testes automatizados.

**`cy.should('contain', 'texto esperado')`**

Usada para verificar se um elemento na página contém o texto especificado durante a execução dos testes automatizados.

**`cy.should('have.class', 'classe esperada)`**

Usada para verificar se um elemento na página possui a classe CSS especificada durante a execução dos testes automatizados.

## Rodando testes com Cypress

### `npx cypress open`
Abre o Cypress Test Runner, onde é possícel executar testes interativamente.

### `npx cypress run`
Executa seus testes em modo headless (sem interface gráfica) e exibe os resultados no terminal.

### `npx cypress run --spec "path_do_spec_especifico"`
Executa um teste específico, fornecendo o caminho para o arquivo de teste.

## Descrição das etapas de preparação de um teste de interface(AngularJS), execução e verificação no Cypress

### Instalação do Cypress

`npm install cypress --save-dev`

### Configuração do Cypress

O Cypress pode ser configurado por meio de um arquivo de configuração (cypress.json) para definir opções como URL base, seletor de elementos padrão, entre outros.

### Estruturação dos testes

Crie uma estrutura de pastas dentro do diretório de testes (geralmente cypress/integration) para organizar os testes. Por exemplo, pode-se ter pastas separadas para diferentes partes da aplicação, como autenticação, perfil do usuário, páginas específicas, etc.

### Escrita dos testes

Em arquivos com a extensão `.cy.ts`, estruture seus testes. Um exemplo simples de teste é o que confere o título da aplicação, que pode ser estruturado da seguinte forma:
``` typescript
describe('Counter', () => {
  beforeEach(() => {
    cy.visit('/');
  });

  it('has the correct title', () => {
    cy.title().should('equal', 'Angular Workshop: Counters');
  });
});
```

### Execução

Para executar os testes em Angular sem a interface do Cypress, basta utilizar o comando: `ng run app-name:cypress-run`.

Para abrir a interface do Cypress a fim de executar os testes em Angular, é possível executar o seguinte comando: `ng run app-name:cypress-open`

### Verificação dos testes no Cypress
Acessando a interface após o comando `cypress-open` indicado, é possível escolher o seu browser(obs: sem suporte para Brave) e acessar a interface. Na aba "Specs", é possível rodar testes ou conjunto deles e acessar o resultado de forma fácil.

Na seguinte imagem, o teste que exemplifiquei para checar o title da aplicação passou, já que está de acordo com 'Angular Workshop: Counters':

<p align="center">
  <img src="assets/print1.png" width="80%">
</p>
