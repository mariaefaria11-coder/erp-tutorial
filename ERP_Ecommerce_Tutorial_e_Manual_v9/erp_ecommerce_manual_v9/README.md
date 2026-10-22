# ERP Commerce — versão completa sem login

Projeto demonstrativo em HTML, CSS e JavaScript puro.

## Estrutura

app/
├── css/
│   └── styles.css
├── js/
│   ├── app.js
│   ├── charts.js
│   ├── data.js
│   ├── theme.js
│   └── tutorial.js
├── html/
│   ├── dashboard.html
│   ├── produtos.html
│   ├── pedidos.html
│   └── clientes.html
└── index.html

## Como executar

Abra `app/index.html` no navegador.

Para melhor funcionamento, também é possível abrir a pasta no VS Code e executar o arquivo com a extensão Live Server.

O sistema abre diretamente no Dashboard, sem login ou autenticação.

## Recursos incluídos

- Dashboard com gráficos de vendas usando Chart.js.
- Gráfico alternativo caso a biblioteca externa não carregue.
- Pesquisa de pedidos por cliente ou número.
- Filtros por Pago, Pendente, Cancelado, Processando e Enviado.
- Cadastro, edição, reposição de estoque e exclusão de produtos.
- Pesquisa de produtos por nome ou SKU.
- Modo claro e modo escuro com preferência salva.
- Responsividade para desktop, tablet e celular.
- Toasts para salvar, editar, excluir, alterar estoque, status e tema.
- Tutorial com tela de boas-vindas.
- Caixa do tutorial posicionada fora do elemento destacado.
- Tutorial contextual em todas as páginas.
- Central de aprendizagem.
- Checklist de tarefas.
- Teste de conhecimento.
- Selo “Usuário preparado” após concluir as etapas necessárias.

## Observação sobre o Chart.js

O dashboard referencia o Chart.js por CDN. Com acesso à internet, os gráficos completos serão exibidos. Se a biblioteca não carregar, o sistema desenha um gráfico alternativo em Canvas.


## Ajuste visual

Esta versão usa uma aparência mais sóbria:
- azul mais fechado;
- menos ciano;
- sombras mais leves;
- menos gradientes;
- menos efeitos de brilho;
- destaque visual mais corporativo.


## Comportamento da trilha

Quando todas as etapas da trilha de aprendizagem forem concluídas, o cartão desaparece automaticamente. A tabela de pedidos recentes passa a ocupar toda a largura disponível.


## Aprendizagem e reinício

- A Central de aprendizagem continua acessível mesmo depois que a trilha desaparece.
- O botão **Reiniciar trilha** apaga apenas o progresso, o tutorial e o resultado do teste.
- Produtos, pedidos e preferência de tema são mantidos nesse reinício.
- O botão **Restaurar dados de demonstração** apaga também as alterações feitas em produtos e pedidos.
- O progresso usa `localStorage`, portanto é específico do navegador e do dispositivo. Em outro computador ou navegador, a trilha começa do zero.
- O teste de domínio agora possui 7 situações práticas e exige 6 acertos.


## VLibras

O widget oficial do VLibras foi incluído nas páginas Dashboard, Produtos, Pedidos e Clientes.

Como utilizar:
1. Clique no botão flutuante do VLibras na lateral da página.
2. Aguarde o avatar carregar.
3. Selecione um texto do sistema para solicitar a tradução para Libras.

O widget é carregado pelo endereço oficial `https://vlibras.gov.br/app/vlibras-plugin.js` e necessita de conexão com a internet.


## Tutorial separado

A aprendizagem agora possui uma página própria:

`app/html/tutorial.html`

Ela contém:

- guia detalhado;
- progresso da trilha;
- atalhos para iniciar o tutorial em cada módulo;
- teste de domínio;
- reinício da trilha;
- restauração dos dados de demonstração.

## GitHub Pages

A versão inclui `index.html` e `.nojekyll` na raiz. Consulte `DEPLOY_GITHUB_PAGES.md`.

## Manual do usuário em documento

O tutorial automático continua ativo no primeiro acesso ao Dashboard. Além dele, esta versão inclui:

- página separada `app/html/tutorial.html`;
- documento Word `documentacao/Manual_do_Usuario_ERP_Ecommerce.docx`;
- botão para baixar o manual dentro da página Tutorial.
