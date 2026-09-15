# Sabores da Casa

Cardápio digital estático da **SABORES DA CASA**, pensado para hospedagem no GitHub Pages. A página usa HTML semântico e CSS puro, com layout mobile-first e cinco produtos oficiais.

## Estrutura

- `index.html`: conteúdo, metadados e cards do cardápio.
- `styles.css`: identidade visual, responsividade e estados de foco nativos.
- `assets/images/`: cinco fotos próprias, uma por produto.

Abra `index.html` diretamente no navegador para visualizar localmente. Para um servidor local, qualquer servidor estático pode servir esta pasta (por exemplo, `python -m http.server`), sem build ou dependências.

## Imagens e identidade

As fotos em `assets/images/` foram geradas com a ferramenta built-in `imagegen`, em proporção 4:3, com marmitas redondas de isopor branco e composição coerente com cada descrição. Para substituir uma foto, mantenha o nome do arquivo (`frango-grelhado.jpg`, `bife-boi.jpg`, `bife-porco.jpg`, `estrogonofe.jpg` ou `frango-batata-frita.jpg`) e a proporção 4:3; o CSS usa `object-fit: cover`.

A logo oficial recebida foi integrada em `assets/images/logo.jpg` sem cortes ou redesenho. O arquivo é usado inteiro no hero, preservando a proporção original.

## Manutenção do cardápio

O preço aparece em cada `.card-meta`. Para alterar o preço, atualize os cinco valores de forma consistente. Para adicionar, remover ou editar um produto, duplique/remova/edite um `<article class="menu-card">` em `index.html`, atualizando também o `alt`, a foto e os campos oficiais. Não adicione dados comerciais que não tenham sido fornecidos.

## GitHub Pages

O repositório está pronto para Pages: publique a raiz da branch principal, sem etapa de build, em **Settings → Pages → Deploy from a branch**. Após o deploy, abra a URL exibida pelo GitHub e confirme que `index.html`, `styles.css` e `assets/images/` carregam. Cada atualização na branch selecionada inicia um novo deploy.

## Validação

Foi feita revisão visual em navegador nos tamanhos 360, 390, 430, 768 e 1440 px: não houve overflow horizontal, as seis imagens carregaram, os cinco preços ficaram visíveis, o grid assumiu 1/2/3 colunas conforme a largura e a âncora `#cardapio` funcionou. A revisão de console não registrou erros ou avisos. As cinco fotos foram conferidas individualmente após o mapeamento final dos arquivos.
