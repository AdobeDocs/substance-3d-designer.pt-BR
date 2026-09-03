---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-14-1.html"
breadcrumb-title: ''
description: Revise as notas de versão do Substance 3D Designer versão 14.1 para saber mais sobre as ferramentas de organização de nós e os novos nós Spline e Caminho.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 14.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versão 14.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 1%

---


# Versão 14.1

Esta atualização apresenta novos recursos para aprimorar o uso diário do Substance 3D Designer: ferramentas de organização de nós para melhorar rapidamente o layout do gráfico, copiar/colar parâmetros para aplicar um conjunto de parâmetros a outro nó e um pino de pixel na exibição 2D para rastrear um pixel específico durante a depuração do gráfico. Ele também adiciona novo conteúdo, principalmente para completar os conjuntos de nós Spline e Caminho.

*Data de lançamento: 14 de janeiro de 2025*

![Dispersão splines em splines](version-14-1.resources/version-14-1-01.png)

## Atualizações de splines e caminhos

As splines e os nós de caminho foram introduzidos na versão 13.0 e, graças ao seu feedback, fizemos um conjunto inicial de aprimoramentos. Primeiro, adicionamos o nó [Splines de Dispersão em Splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-splines-splines/scatter-splines-on-splines.md), que distribui splines ao longo de uma spline pai, oferecendo opções semelhantes às de um nó de dispersão normal. Além disso, o nó [Máscara para caminhos](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) foi aprimorado para dar mais controle sobre a posição do primeiro vértice no caminho. Também possibilitamos introduzir a aleatoriedade no nó [Lista de pontes de spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dispersão Spline na animação de Spline 1](version-14-1.resources/version-14-1-02.gif){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dispersão splines nas splines 2](version-14-1.resources/version-14-1-03.gif){zoomable="yes"}

</td>
</tr>
</table>

## Ferramentas de alinhamento de nós

Se você deseja manter um gráfico limpo e legível, as [ferramentas de alinhamento de nó](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md) foram feitas para você e foram completamente renovadas! Agora é possível espaçar uniformemente os nós (horizontal ou verticalmente), e alinhar os nós evita qualquer sobreposição empilhando-os de maneira adequada. Cherry no topo: ambos os recursos levam o tamanho real dos nós em consideração!

![Alinhar nós](version-14-1.resources/version-14-1-04.gif){zoomable="yes"}

## Copiar/colar parâmetros

Agora é possível [copiar os parâmetros de um nó e colá-los em outro](../../compositing-graphs/manage-parameters/manage-parameters.md), de modo que todos os parâmetros correspondentes no nó de destino serão atualizados para os valores do nó de origem. Isso é muito útil se, por exemplo, você deseja transportar os parâmetros de um nó de cor para sua versão em tons de cinza ou vice-versa. (por exemplo, o nó Tile Sampler)

## Fixar o pixel na visualização 2D

A nova [ferramenta Color Sampler](../../interface/2d-view/color-sampler/color-sampler.md) no modo de exibição 2D permite rastrear o valor de um pixel selecionado, soltando um pino nele. Isso é muito útil para garantir que você esteja sempre visualizando as informações do mesmo pixel em vários nós em um gráfico. Abra o painel Informações para acessar a ferramenta e experimente.

![Classificador de cores: usando a ferramenta](version-14-1.resources/version-14-1-05.gif "Classificador de cores: usando a ferramenta"){width="640px" zoomable="yes"}

## Melhorias na pesquisa

A ferramenta [localizador de nós](../../interface/the-graph-view/node-finder/node-finder.md) foi ligeiramente aprimorada:

* Agora você pode ativar um modo recursivo para uma pesquisa mais profunda;
* O modo difuso pode ser desativado se você quiser procurar um termo exato;
* O foco é automaticamente definido no campo de pesquisa ao ativar a ferramenta de localização de nós;
* O layout da barra de ferramentas foi repensado para economizar espaço.

![Barra de ferramentas de pesquisa](version-14-1.resources/version-14-1-06.png){width="640px"}

## Vídeos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![splines de dispersão de vídeo nas splines](version-14-1.resources/version-14-1-07.png)](https://www.youtube.com/watch?v=aUUWV1dYQdI)

</td>
<td style="border: 0;" valign="top">

[![recursos de experiência do usuário de vídeo](version-14-1.resources/version-14-1-08.png)](https://www.youtube.com/watch?v=LwexybAEjaI)

</td>
</tr>
</table>

## Notas de versão

### 14.1.0

*(Lançado em 14 de janeiro de 2025)*

### Adicionado

* [Exibição 2D] Adicionar exibição de pixels fixados no painel Informações
* [API] Expor o tamanho da caixa de nós na cena da Exibição de gráfico
* [Content] &#39;Mesclagem de Height de material&#39;: adicionar saída de &#39;Máscara de Height&#39;
* [Content] &#39;Processador de Vértice de Caminho&#39;: Use o botão &#39;Editar função&#39; para o parâmetro &#39;Função por vértice&#39;
* [Conteúdo] Níveis automáticos: limpar parâmetro não utilizado, ajustar rótulos e dica de ferramenta
* [Conteúdo] Mascarar para caminhos v2
* [Conteúdo] Novo nó de MLV (Média da Menor Variação)
* [Content] Novo nó Filtro Mediano
* [Content] Quantificar cor: adicionar uma opção de filtragem “Mais próximo”
* [Content] Lista de pontes de spline: adicionar parâmetros de deslocamento de spline aleatórios
* [Content] Ferramenta de linha flexível: Novo nó de Spline (Quadrático)
* [Content] Triangle Grid: alterar método de triangulação e usar loops
* [Content] Nova Dispersão de Splines no nó Splines
* [Cooker] Expor parâmetro base &#39;Pixel ratio&#39; como variável estática &#39;$pixelratio&#39;
* [CrashReport] Integrar nova janela de relatório de falhas
* [Engine] Adicionar a versão Vulkan/Metal do mecanismo de mesclagem
* [Graph] Modo de material: permite a conexão com a entrada sem uso quando um único link é selecionado
* [Graph] Link de material: permitir conexões padrão quando a conexão não for ambígua
* [Gráfico] Ferramentas de alinhamento de nós: adicionar distribuições horizontais/verticais, alinhamentos à esquerda/direita/superior/inferior e suportar nós empilhados
* [Biblioteca] Corrigir cor do texto em menus contextuais
* [Parâmetros] Copiar parâmetros de um nó para outro
* [Propriedades] “Redefinir tudo”: remove a janela pop-up de confirmação
* [Recursos] Defina o formato como “Todos os formatos” na caixa de diálogo “Vincular bitmap”
* [Pesquisar] Adicionar uma maneira de ativar/desativar um modo recursivo
* [Pesquisar] Adicionar uma maneira de habilitar/desabilitar a pesquisa difusa
* [Search] Sempre mostrar e definir o foco no campo de termo de pesquisa ao ativar o Localizador de nós usando seu atalho de teclado
* [Pesquisar] Reprocessar a opção de filtro
* [Atalhos] Permitir que as teclas &#39;V&#39;, &#39;H&#39; e &#39;S&#39; sejam atribuídas
* [Terceiro] Atualize para o Qt 6.5.7
* [UX] As caixas de diálogo modais não devem ser minimizáveis
* [UX] Remover rolagem horizontal na caixa de diálogo de alerta

### Correções

* [Conteúdo] Chanfro: o formato normal não é afetado pela preferência global
* [Conteúdo] O nó Cor para máscara não ignora o alfa
* distância direcional [Content]: resultado incorreto quando a entrada tem uma proporção de imagem vertical
* [Content] Mapeador de Flood Fill: aviso gerado para variável ausente
* [Content] Computação de histograma: o resultado é 16 vezes o que deveria ser
* [Conteúdo] A cáustica de IR não funciona em resolução não quadrada
* [Content] Lista de pontes de spline: resultado incorreto ao usar deslocamentos de Início/Fim
* [Conteúdo] Seleção de spline: a quantidade de spline de saída pode ser maior que a quantidade de spline de entrada
* [Conteúdo] Distorção de spline produz um resultado em preto com o mecanismo SSE
* [Content] Triangle Grid: o padrão não está posicionado adequadamente no lado a lado
* [Content] Triangle Grid: A divisão em blocos gráficos é interrompida em um caso específico
* [Data] Falha ao alterar o identificador de entrada do gráfico em um caso específico
* [Gráfico de funções] Valores longos aparecem sobrepostos em nós &#39;Float&#39;
* [Fx-Map] Falha ao exibir as propriedades do nó Quadrante
* [Graph] [UDIM] Ter uma barra de rolagem na lista UDIM resulta em entradas 1..1 1..2
* [Graph][Atalhos] O nó criado usando um atalho não é colocado em um link existente após a duplicação do nó
* [Propriedades] Exibição incorreta de parâmetro quando o valor é inválido
* [Publish] As dependências recíprocas resultam em um loop infinito ao publicar um pacote
* [Publish] Falha silenciosa ao usar a ação &#39;Publish&#39; no pacote com dependência descarregada
* [UI] O widget “Tamanho do pai” não é exibido corretamente quando expandido e pode bloquear a interface (somente no macOS)
* [IU] A janela principal fica atrás de outros aplicativos em alguns casos (somente Windows)
