---
source-git-commit: e44437dcecf30714ffe5274c91135d84a0360aa7
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---
# CLAUDE.md

Este arquivo fornece orientação para o código Claude (claude.ai/code) ao trabalhar com código neste repositório.

# Documentação do Substance 3D Designer

Esse repositório contém a documentação do Substance 3D Designer. Não há código de aplicativo, etapa de compilação ou conjunto de testes — o repositório *é* o conteúdo, escrito em Markdown e publicado no [Adobe Experience League](https://experienceleague.adobe.com/docs/substance3d-designer.html?lang=en).

# Estrutura do repositório

* `help/` — todo o conteúdo da documentação, organizado para espelhar o sumário.
* `help/guide/TOC.md` — o sumário. Cada entrada é um link relativo (com raiz em `/help/...`) para o arquivo Markdown de uma página. `TOC.md` também transporta metadados de árvore de páginas (`user-guide-title`, `breadcrumb-title`, `nudge`, âncoras de seção como `{#section-id}`).
* `help/assets/` — pasta de imagem compartilhada herdada. A mídia específica da página agora reside em uma pasta irmã `<md-file-name>.resources/` por página (consulte a convenção de pasta/sumário abaixo). Apenas algumas imagens restantes não referenciadas por nenhuma página ainda estão aqui. Coloque novas imagens na pasta `.resources` da página de uso, não aqui.
* `help/glossary/glossary.md` — uma única página de glossário grande, organizada em ordem alfabética com extensões de âncora (`<span id="term"></span>`) usadas para vinculação cruzada via fragmentos `#term`.
* `metadata.md` — assunto principal no nível do repositório (nuvem/solução/IDs de produto, `git-repo` etc.) herdado por cada `TOC.md`. Edite isso apenas para alterações de metadados em todo o repositório; os metadados específicos da página pertencem ao próprio tema principal da página.
* `redirects.csv`, `linkcheckexclude.json`, `markdownlint_custom.json`, `pipeline.opts` — configuração de publicação de pipeline (redirecionamentos, exceções de verificação de link, substituições de regra de link, opções de pipeline).
* `fix-image-names.py` — utilitário único que renomeia `help/assets` imagens com sufixos entre parênteses (por exemplo, `foo(1).png` → `foo_1.png`) e regrava cada referência de Markdown para corresponder. Não faz parte de nenhum fluxo de trabalho regular; execute manualmente somente quando esses nomes de arquivo reaparecerem.

## Convenção de pasta/sumário

Para cada entrada em `help/guide/TOC.md`:
* Há uma pasta correspondente em `help/`, seguindo o mesmo aninhamento do sumário.
* Essa pasta contém um arquivo Markdown, nomeado como a versão de caso kebab do título da página.
* Se a página tiver mídia personalizada (imagens, GIF, vídeos), ela estará em uma subpasta irmã chamada `<md-file-name>.resources`.

Ao adicionar ou mover uma página, atualize `TOC.md` e o layout da pasta juntos. Eles devem permanecer sincronizados.

## Páginas de referência do nó

As árvores de biblioteca de nós (por exemplo, `help/compositing-graphs/nodes-reference-for-com/node-library/<category>/<node>/<node>.md`) são um tipo de página distinto com seu próprio layout consistente: uma tabela de HTML de ícone/descrição, seguida pelas tabelas `## Inputs` / `## Outputs` / `## Parameters` ancoradas (`#inputs`/`#outputs`/`#parameters`) e uma galeria `## Examples`. Eles usam o front matter **mínimo** (somente `title` + `description`), não o bloco de página de conteúdo regular abaixo — modelado em `.../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md`. A mídia incorporada (ícone, exemplo, imagens/GIF) está em uma pasta irmã `<node-name>.resources/` ao lado da página, mencionada relativamente. Use a habilidade `generate-node-documentation` (se houver) para o modelo de criação completo.

## Assunto frontal da página

As páginas de conteúdo normal usam um bloco de front matter como:

```yaml
---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/<section>/<page>.html"
breadcrumb-title: ""
description: <one/two sentence SEO description>
helpx_creative_field: ""
helpx_description: Designer > <Section> > <Page>
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: <Page title>
user-guide-description: ""
user-guide-title: ""
---
```

Mantenha o `description` preciso e conciso. Ele é usado para fragmentos de SEO/pesquisa.

# Regras de criação de conteúdo

* O inglês é a fonte da verdade; todas as outras línguas são traduzidas a partir dele.
* Todos os links para outras páginas de documentação devem ser links **relativos**; todos os links para recursos externos devem ser links **absolutos**.
* O conteúdo é escrito em Markdown com a variante GitHub com extensões personalizadas de Experience League/pegadinhas, documentado [aqui](https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown). Use a habilidade `write-experience-league-markdown` (se houver) para os detalhes.
* Cada alteração enviada passa por verificações de linha automatizadas e validação de link no IC (veja abaixo) — verifique `markdownlint_custom.json` e `linkcheckexclude.json` antes de assumir que uma regra se aplica ou que um link precisa de correção.

# Validação/CI

* O `.github/workflows/validate-articles.yml` é executado em PRs e envia por push para `main` (e por meio de um comentário de PR do `retest`), chamando o fluxo de trabalho reutilizável do `Adobe-Enterprise-Docs/workflows` compartilhado para lint Markdown e validar links. Não há script equivalente local neste repositório — o IC é a fonte confiável para aprovação/reprovação.
* `.github/workflows/mirror.yml` espelha `main` para o repositório público no push; é infraestrutura, não algo que as alterações de conteúdo precisam tocar.
* O `markdownlint_custom.json` estende o conjunto de regras `markdownlint.json` compartilhado e desabilita várias regras (MD005, MD007, MD018, MD032, MD033, MD034, MD037, MD040) que entram em conflito com as extensões de Markdown personalizadas do Experience League (por exemplo, HTML embutido, ênfase não padrão). Não “corrija” o conteúdo para atender a essas regras desativadas.
* `linkcheckexclude.json` lista branca de padrões de links (atualmente `example.com`/`example-end.com`) que o verificador de links deve ignorar.

# Convenções de trabalho

* Esta é uma documentação pesada de notas de versão — as notas de versão ficam em tempo real em `help/release-notes/`, uma pasta por versão (por exemplo, `version-16-0`), mais as páginas de agregação `all-changes` e `old-versions`. Siga a pasta da versão existente como um modelo ao adicionar uma nova versão.
