---
name: write-experience-league-markdown
description: |
  Regras de sintaxe, extensões personalizadas e especificações para escrever o conteúdo de Markdown publicado no Adobe Experience League. Use essa habilidade sempre que criar ou editar qualquer página sob ajuda/neste repositório (ou qualquer outro repositório de conteúdo de Experience League): títulos, links, imagens, tabelas, blocos de nota/alerta, tags UICONTROL/DNL, incorporações de vídeo, âncoras e armadilhas de renderização conhecidas. Fonte: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 4%
---

# Gravando Markdown de Experience League

O Experience League renderiza o Markdown com sabor de GitHub por meio de um pipeline personalizado
com suas próprias extensões e peculiaridades de renderização. A GFM padrão funciona na maioria das vezes, mas
os itens abaixo são específicos do Experience League — interprete-os incorretamente e apresente seu conteúdo
falha no IC de verificação de link/link ou é renderizado incorretamente no site ativo.

## Títulos

* `#` a `#####` (níveis 1-5). O assunto principal `title` da página é
efetivamente nível 0; a primeira rubrica de redução no corpo deve ser uma
um único cabeçalho `# Level 1` que corresponda (ou que corresponda de perto) ao título da página.
* Não ignore níveis arbitrariamente; o miniTOC é gerado a partir de títulos.

## Formatação de texto

* `**bold**`, `*italic*`, `***bold and italic***`.
* Escape caracteres especiais literais com uma barra invertida (`\*`, `\_`, etc.).
* **E/s comercial** em títulos/títulos deve ser escrito(a) (`and`) ou codificado(a) como
  `&amp;` — um `&` bruto em um título pode interromper a análise.
* **Os colchetes angulares** usados como texto literal (não HTML real) devem ser codificados:
  `<placeholder>` → `&lt;placeholder&gt;`.
* **Aspas inteligentes** coladas de processadores de texto devem ser codificadas, e não deixadas como
caracteres curvos literais: `&#8220;` duplo esquerdo, `&#8221;` duplo direito,
apóstrofo/direito único `&#8217;`.

## Listas

* Listas numeradas: iniciar cada item com `1.` (ou `1)`) — GitHub/Experience
Números automáticos da liga, independentemente dos dígitos literais digitados.
* Listas com marcadores: use `*`, `-` ou `+`, mas **não combine marcadores
na mesma lista/documento**.
* O aninhamento de lista `TOC.md` usa `+` de forma consistente — siga o arquivo existente
estilo de marcador em vez de introduzir um diferente.

## Vínculos

* As referências cruzadas internas devem ser links de Markdown **relativos** para o
arquivo de destino `.md`: `[Overview](../../overview.md)`.
* As referências externas devem ser URLs **absolutas**.
* Ancora nos títulos/intervalos de outra página: anexar `#anchor-id`, por exemplo.
  `[Mesh](../../glossary/glossary.md#mesh)`.
* As âncoras na página são declaradas como um título (com espaçador automático) ou um
`<span id="anchor-id"></span>` (HTML) / `{: #anchor-id}` (Markdown) explícito imediatamente antes do termo —
consulte `help/glossary/glossary.md` para saber o padrão usado em todo este repositório.
* As âncoras de seção `TOC.md` usam a sintaxe `{#section-id}` após um cabeçalho/lista
rótulo, por exemplo, `Getting started{#getting-started}`.

## Imagens

Use a sintaxe de imagem de Markdown sempre que possível:

```markdown
![Alt text](path/to/image.png "Optional hover text")
```

* O texto `![...]` é um texto alternativo acessível obrigatório. Seja conciso e faça
não use sublinhados; use espaços ou hífens.
* O caminho da imagem pode ser relativo ao arquivo Markdown ou relativo à raiz, como
como `/help/assets/shared-image.png`. Imagens específicas de uma página pertencem à
pasta irmã `<page-name>.resources/` (por exemplo,
  `<page-name>.resources/image.png`). `help/assets/` é uma pasta compartilhada herdada;
  não adicione novas imagens específicas da página.
* Parâmetros opcionais de consulta de imagem podem controlar o processamento de CDN:
  `?width=750&format=png&optimize=medium`. Manter estes parâmetros na imagem
  URL, antes de qualquer bloco de propriedades.
* Adicionar propriedades de imagem imediatamente após `)` de fechamento:
  `![Alt text](image.png "Hover text"){width="300" align="center"}`.
  `width` é um valor de pixel ou uma porcentagem da área de exibição; escala das imagens
proporcionalmente. Os valores de alinhamento com suporte são `center` e `right`.
  Não há suporte para `valign`.
* Use `modal="regular"` ou `zoomable="yes"` para fazer uma imagem com clique para aplicar zoom:
  `![Alt text](image.png){width="100" zoomable="yes"}`. Não combinar
  clique para aplicar zoom com um link de imagem; o hiperlink tem prioridade.
* Para criar um link de imagem para outra página, envolva a imagem em um link de Markdown:
  `[![Alt text](image.png)](../target/target.md)`.
* Para imagens grandes, forneça pelo menos 640 pixels de largura de origem quando prático,
usar no máximo 2.000 pixels, a menos que necessário, e manter os arquivos de imagem sob
5 MB onde possível. O pipeline aceita arquivos de até 100 MB, mas os arquivos acima
Falha de validação de 20 MB e os artigos geralmente não devem conter mais de
100 imagens (algumas orientações mais antigas dizem 200; use o limite mais restrito).

Use HTML somente quando Markdown não puder expressar o layout necessário, como um
uma tabela especial ou uma apresentação embutida personalizada. O formulário de imagem de HTML compatível
é:

```html
<img src="image.png" alt="Alt text" />
```

* Sempre forneça um atributo `alt` significativo e use um ou relativo
`src` relativo à raiz consistente com imagens de Markdown.
* Para imagens HTML dentro do HTML incorporado preservado, adicione
  `data-preserve-html="true"` para as marcas contentoras quando exigido pelo
  marcação ao redor. Por exemplo:

  ```html
  <div data-preserve-html="true" align="center">
    <img src="my-page.resources/preview.gif" alt="Preview" />
  </div>
  ```

* Para ativar o clique para aplicar zoom em uma imagem de HTML, use
  `class="modal-image"` na marca `<img>`.
* Não use atributos de HTML sem suporte ou confie em `valign`; prefira Markdown
propriedades para largura e alinhamento.

## Tabelas

Preferir tabelas de Markdown nativas para conteúdo tabular comum:

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

* Coloque uma linha em branco antes da tabela. As tabelas de markdown exigem pelo menos um
linha de cabeçalho e uma linha de corpo; usar uma tabela HTML para uma linha única ou sem cabeçalho
tabela.
* Use pelo menos três hifens em cada célula separadora de cabeçalho e mantenha a mesma
número de caracteres de pipe em cada linha. Escape um pipe literal como `\|` ou
  `&vert;`.
* Use marcadores de alinhamento na linha separadora quando necessário:
  `|---|:---:|---:|` para alinhamento à esquerda, ao centro e à direita.
* O HTML incorporado é compatível com células de tabela de Markdown para quebras de parágrafo e
listas básicas. Use `<p>` para parágrafos separados, `<br>` para quebras de linha e
  `<ul>`/`<ol>` com `<li>` itens para listas. Adição
  `data-preserve-html="true"` para elementos de HTML embutidos quando exigido pelo
  marcação do repositório adjacente.

  ```markdown
  | Header | Details |
  |---|---|
  | Text | First paragraph.<p>Second paragraph.<br>New line.<ul><li>Item</li></ul> |
  ```

* Evite mesas muito largas e muito altas; elas são difíceis de navegar.
Tenha cuidado com o código incorporado nas tabelas, pois códigos longos podem forçar
larguras de coluna desproporcionadas.
* Para escolher o layout de tabela para uma tabela de Markdown, adicione a propriedade após a
tabela, separada por uma linha em branco:

  ```markdown
  {style="table-layout:fixed"}
  ```

  Use `table-layout:auto` (o padrão) quando o texto longo ou o código precisar de flexibilidade
  larguras de coluna. Use `fixed` para colunas balanceadas, como tabelas que contêm
  imagens de tamanho semelhante.

Use uma tabela HTML quando Markdown não puder expressar a estrutura necessária, como
omissão de cabeçalhos, combinação de células com extensões, equilíbrio de colunas ou alinhamento
conteúdo dentro das células:

```html
<table style="table-layout:fixed">
  <tr>
    <th>Property</th>
    <th>Value</th>
  </tr>
  <tr>
    <td align="center">Example</td>
    <td>Details</td>
  </tr>
</table>
```

* Os elementos de tabela com suporte incluem `<table>`, `<tbody>`, `<thead>`, `<tfoot>`,
  `<tr>`, `<th>`, `<td>`, `<col>` e `<colgroup>`, juntamente com os itens com suporte
elementos embutidos, como `<p>`, `<br>`, `<b>`, `<i>`, `<ul>`, `<ol>` e
  `<li>`.
* Não use a sintaxe de Markdown dentro de uma tabela de HTML. Por exemplo, Markdown
notas, imagens e links podem ser renderizados literalmente. use a sintaxe de HTML em vez disso.
  As marcas de localização `UICONTROL` e `DNL` são exceções.
* Use `align="left"`, `align="center"` ou `align="right"` em uma célula quando
necessário. As tabelas HTML não podem conter tabelas aninhadas.
* Defina o layout da tabela HTML na tag de abertura:
  `<table style="table-layout:auto">` ou
  `<table style="table-layout:fixed">`.
* Para uma tabela de HTML de uma linha sem bordas, use
  `<tr style="border: 0;">`.

## Código

* Código incorporado: mochilões únicos.
* Blocos cercados: triplos backticks, com uma linguagem opcional para sintaxe
realçando (` `&#x200B;``python `, ` ``&#x200B;`javascript ` etc.).

## Blocos de notas/alertas

Sintaxe de blockquote personalizada, um tipo por bloco, linha de blockquote em branco entre
a etiqueta e o corpo:

```markdown
>[!NOTE]
>
>This is a standard NOTE block.

>[!TIP]
>
>This is a standard TIP.

>[!IMPORTANT]
>
>This is an IMPORTANT note.
```

Tipos com suporte: `NOTE`, `TIP`, `IMPORTANT`, `CAUTION`, `WARNING`,
`ADMINISTRATION`, `AVAILABILITY`, `PREREQUISITES`, `ERROR`, `INFO`, `SUCCESS`.

## Incorporações de vídeo

O Experience League não oferece suporte a incorporações diretas de vídeo MP4 ou YouTube em `[!VIDEO]` blocos. Se precisar de uma visualização animada, use um GIF na pasta irmã da página `.resources` e centralize-o com um HTML embutido, se necessário.

```markdown
<div data-preserve-html="true" align="center">
  <img src="my-page.resources/my-preview.gif" alt="My preview" />
</div>
```

Não usar `[!VIDEO]` para arquivos MP4 locais, arquivos MP4 remotos ou URLs do YouTube — o pipeline de publicação os rejeita e o IC falha.

## tag UICONTROL

Quebra os nomes de elementos da interface do usuário (rótulos de botões, itens de menu, nomes de campos) em linha, de modo
o pipeline de localização sabe como verificar uma cadeia de caracteres traduzida e cai
voltar para o rótulo em inglês, se não existir nenhum:

```markdown
Click [!UICONTROL Save] to apply changes.
Go to [!UICONTROL Tools] > [!UICONTROL Settings].
```

Use-o para cada rótulo literal da interface do usuário mencionado no texto de instrução (menu
itens, nomes de botões, títulos de diálogo, nomes de painéis).

## Tag DNL (”Não Localizar”)

Empacota nomes de produtos, nomes de recursos de terceiros ou qualquer frase que deva
nunca seja traduzido automaticamente:

```markdown
Use [!DNL Adobe Analytics] to track metrics.
The [!DNL Target] implementation requires configuration.
```

Neste repositório, use-o para nomes de produtos como `[!DNL Substance 3D Designer]`,
`[!DNL Substance 3D Sampler]`, etc., nas primeiras menções/menções proeminentes por página,
consistente com as páginas existentes.

## HTML em linha

O HTML bruto é permitido (este repositório `markdownlint_custom.json` desabilita MD033
especificamente por esta razão), mas só é fiavelmente preservada através da
pipeline quando as marcas carregam `data-preserve-html="true"`. Reservar HTML in-line
para casos em que o Markdown simples não pode expressar (imagens/listas dentro de células da tabela,
`<span id="...">` âncoras) em vez de substituí-las pelo Markdown.

## Matéria frontal

Consulte a seção “Page front matter” do AGENTS.md para obter o bloco exato usado pelo
páginas de conteúdo regular neste repositório e `metadata.md` no nível de repositório
herdados.