---
name: write-experience-league-markdown
description: ""
Source: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: e44437dcecf30714ffe5274c91135d84a0360aa7
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 6%

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
`<span id="anchor-id"></span>` explícito imediatamente antes do termo —
consulte `help/glossary/glossary.md` para saber o padrão usado em todo este repositório.
* As âncoras de seção `TOC.md` usam a sintaxe `{#section-id}` após um cabeçalho/lista
rótulo, por exemplo, `Getting started{#getting-started}`.

## Imagens

* `![Alt text](path/to/image.png "Optional hover title")`.
* Parâmetros de consulta de dimensionamento/otimização opcionais são compatíveis:
  `![Adobe logo](my-page.resources/logo.png?width=750&format=png&optimize=medium)`.
* **O texto alternativo não deve conter sublinhados**; eles não são renderizados corretamente;
em vez disso, use hifens ou espaços.
* Imagens específicas de página ficam em uma pasta irmã `<page-name>.resources/`
ao lado de `.md`, com referência relativa (por exemplo,
  `<page-name>.resources/image.png`). `help/assets/` é um legado compartilhado
  — não adicione novas imagens (consulte CLAUDE.md).

## Tabelas

* Delimitado por pipe, com uma linha de separação de cabeçalho de hífen:

  ```markdown
  | Header | Another header | Yet another header |
  |--- |--- |--- |
  | row 1 | column 2 | column 3 |
  | row 2 | row 2 column 2 | row 2 column 3 |
  ```

* Uma linha em branco deve preceder a tabela ou ela não será renderizada como uma tabela.
* As tabelas não podem conter conteúdo de bloco complexo ou de vários parágrafos de forma limpa em um
célula — onde este repositório precisa de imagens/listas dentro de uma célula de tabela (por exemplo,
tabelas de comparação em `overview.md`), ele volta para HTML embutido
(`<div>`, `<b>`, `<ul>`/`<li>`) com `data-preserve-html="true"` em cada
para que o pipeline não o retire. Siga esse padrão existente em vez de
do que inventar um novo HTML em linha, a menos que seja necessário.

## Código

* Código incorporado: mochilões únicos.
* Blocos cercados: triplos backticks, com uma linguagem opcional para sintaxe
realçando (` ```python `, ` ```javascript ` etc.).

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

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

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

Consulte a seção “Page front matter” do CLAUDE.md para obter o bloco exato usado pelo
páginas de conteúdo regular neste repositório e `metadata.md` no nível de repositório
herdados.