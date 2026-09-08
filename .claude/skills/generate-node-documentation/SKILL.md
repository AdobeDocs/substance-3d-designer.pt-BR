---
name: generate-node-documentation
description: ""
source-git-commit: 475af5f27b827f66289993dbd8367904c1baf42b
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 4%

---


# Gerando documentação de nó

Cada página de referência de nó folha neste repositório segue uma estrutura consistente. Este
habilidade é a especificação para essa estrutura. O exemplo canônico e completo é
`.../node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md` —
na dúvida, abra-o e espelhe-o.

Esta habilidade abrange somente a *estrutura* de página de nó. Para Markdown de Experience League base
(blocos de nota/alerta, links relativos versus absolutos, UICONTROL/DNL, parâmetros de consulta de imagem,
lint gotchas) siga a habilidade `write-experience-league-markdown`.

## Onde fica uma página de nó (convenção de pasta / sumário)

* Uma pasta por nó, no caminho da categoria/subcategoria correspondente, por exemplo
  `.../node-library/<category>/<subcategory>/<node-name>/<node-name>.md`.
* A pasta é nomeada como o título do nó kebab-case; ela contém o arquivo **one** `.md`
nomeados de forma idêntica.
* Todas as mídias incorporadas para a página (ícone, imagens de exemplo, GIF) estão em um irmão **  `<node-name>.resources/` pasta **ao lado de `.md` e são referenciadas com um
  caminho relativo (por exemplo, `<node-name>.resources/<file>.png`). Não aponte páginas de nó para
  a pasta compartilhada `help/assets/`, que é um padrão herdado sendo descontinuado; novo e
  as páginas editadas usam sua própria pasta `.resources`.
* Cada página tem uma entrada correspondente em `help/guide/TOC.md`. Ao adicionar ou mover um
, atualize `TOC.md` e o layout da pasta juntos (consulte a seção de pastas/sumário do CLAUDE.md
convenção).

## Matéria frontal

As páginas de nó usam o bloco **mínimo** — somente `title` e um estilo de navegação estrutural
`description`. (Isso é diferente dos documentos do bloco legado de 11 campos CLAUDE.md para
páginas de conteúdo normal.)

```yaml
---
title: "Shape splatter v2"
description: "Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Generator > Pattern > Shape splatter v2"
---
```

## Estrutura do corpo

De cima para baixo, tudo abaixo da matéria da frente:

### &#x200B;1. Título H1

Um único `# <Node title>` — exatamente um H1 por página.

### &#x200B;2. Tabela de ícones/descrições

Uma tabela de HTML, uma linha, duas células. A célula esquerda (`33.33%`) contém o ícone e, em seguida, o
`In:` navegação estrutural; a célula direita (`100.00%`) contém `## Description` e a prosa.

```html
<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![<Node title> icon](<node-name>.resources/<node-name>.png "<Node title>")

<b>In:</b> <Category> &gt; <Subcategory>

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

<Description prose.>

</td>
</tr>
</table>
```

Convenções de prosa de célula de descrição:
* Separe os parágrafos com `<br><br>` (linhas em branco brutas dentro da célula não são confiáveis).
* A ênfase embutida é `<b>…</b>` / `<i>…</i>`.
* Os auxiliares de introdução usam `<i>Note:</i>` / `<i>Tip:</i>` no início da frase.
* Use `&gt;` para `>` na linha `In:` (está dentro do HTML). Use a categoria /
nomes de subcategorias do próprio nó; não os invente.

### &#x200B;3. Chamadas opcionais

`>[!INFO]`, `>[!TIP]`, `>[!NOTE]`, etc. vá **depois** da tabela de ícone/descrição (não
dentro da célula). Sintaxe por habilidade `write-experience-league-markdown`.

### &#x200B;4. Entradas

Incluir somente se o nó tiver fixares de entrada. Preceda o título com uma âncora.

```markdown
<a name="inputs"></a>

## Inputs

|  |  |
|:---|:---|
| <b>Background height</b> <i>Grayscale</i> | The base height map in which shapes are scattered.<br><br>The contribution is controlled by the <b>Background input opacity</b> parameter. |
```

* Duas colunas, linha de cabeçalho vazia, alinhamento de `|:---|:---|`.
* Uma linha por entrada: célula esquerda `<b>Name</b> <i>Type</i>`, célula direita a descrição.
* O marcador de tipo é HTML itálico — `<i>Type</i>` — não markdown `*Type*`.

### &#x200B;5. Saídas

Mesma forma das Entradas, com `<a name="outputs"></a>` + `## Outputs`. Incluir somente se o
nó documenta saídas distintas (muitos nós têm uma única saída implícita e omitem isso)
seção — não invente uma).

Para saídas multicanal compactadas, quebre os canais com `<br>` e recue
subpontos com `&nbsp;` (consulte as linhas “Splatter UVW” / “Dados de respingos” no
referência):

```markdown
| <b>Splatter UVW</b> | <b>R</b> - U component of the shapes' UVs.<br><b>G</b> - V component of the shapes' UVs.<br><b>B</b> - The shapes' height. (W)<br><b>A</b> - Packed data:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- <i>Integer part:</i> The shapes' unique identifier. |
```

### &#x200B;6. Parâmetros

Mesma forma de tabela, com `<a name="parameters"></a>` + `## Parameters`. Omitir tudo
se o nó não tiver parâmetros (nunca emita uma tabela vazia ou um “Sem parâmetros”).
linha).

* **Parâmetros agrupados**: emita uma linha de rótulo de abrangência com uma célula direita vazia antes do
linhas do grupo:

  ```markdown
  | <b>Positioning</b> |  |
  | <b>Project Input</b> <i>UV Position, World Space Position</i> | Choose whether the projection position is set in 2D/UV or in 3D/World space. |
  ```

* **Valores de enumeração / várias opções**: liste as opções dentro da célula de descrição como uma
  Lista de traços separados por `<br>`:

  ```markdown
  | <b>Position distribution mode</b> <i>Integer</i> | The method of distributing the shapes:<br><br>- <b>2D grid:</b> A simple uniform grid.<br>- <b>Poisson disc:</b> Randomly offsets grid cells to prevent overlaps.<br>- <b>Uniform:</b> An even distribution of a set number of shapes. |
  ```

### &#x200B;7. Exemplos

Inclua apenas se houver imagens/GIF de exemplo. Usar uma tabela de galeria de HTML; uma `<td>`
por imagem com uma legenda opcional; quebra para uma nova `<tr>` após 3 imagens. Caminhos de mídia
aponte para a pasta `.resources` da página.

```html
## Examples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file>.gif" /><br><i>Caption</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./<node-name>.resources/<file2>.jpg" /><br><i>Another caption</i>
        </td>
    </tr>
</table>
```

Deixe as células à direita em uma linha final parcialmente preenchida vazias (`<td …></td>`) em vez de
refluxo. Omitir legendas se a origem não tiver nenhuma.

## Valores do tipo canônico

Reutilizar a palavra de tipo do próprio nó; valores típicos: `Grayscale`, `Color`, `Integer`,
`Float`, `Float2`, `Float3`, `Float4`, `Integer2`, `Boolean`, `Grayscale Input`,
`Color Input`, `(Color value)`, `(Grayscale value)`. Não inventar ou “normalizar” um tipo
o nó realmente não usa.

## Regras de célula de tabela

* Nenhuma nova linha bruta dentro de uma célula de tabela — une linhas com `<br>` (e `<br><br>` entre
parágrafos).
* A ênfase dentro das células é `<b>`/`<i>`, e o marcador de tipo é sempre `<i>Type</i>`.
* Recuar subpontos aninhados com `&nbsp;` sequências.

## Regras / não

* **Não fabricar** Entradas, Saídas ou Parâmetros que o nó não tem; omita o
em vez disso. Não reformule, resuma ou elimine conteúdo técnico existente — apenas
reformate-o.
* **Manter vínculos relativos** para outras `.md` páginas; vínculos externos absolutos.
* **Descartar o antigo croft** ao editar uma página antiga neste formato: marcas de dificuldade
(`**Simple**` / `**Intermediate**` / `**Complex**`), o `## <Title>`
subtítulo dentro da célula do ícone, frases stub como “Não há imagens anexadas a
esta página.” e qualquer tabela de navegação/wrapper vazia restante de migrações anteriores.
* **Um H1** por página; as seções usam `##` e as âncoras Inputs/Outputs/Parameters
(`inputs` / `outputs` / `parameters`) devem preceder seus cabeçalhos para que entre páginas
  `#inputs` links resolvidos.
* **Mantenha `TOC.md` sincronizado** ao adicionar, renomear ou mover uma página.
