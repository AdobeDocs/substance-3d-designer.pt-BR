---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/interface/3d-view/material-properties.html"
breadcrumb-title: ''
description: Configure as propriedades do material na visualização 3D para visualizar e ajustar como os materiais da Substance aparecem em objetos 3D.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Material properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Propriedades do material
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 29%

---


# Propriedades do material

A [Exibição 3D](../../../interface/3d-view/3d-view.md) renderiza a superfície dos modelos usando um programa chamado *sombreador*. O sombreador define o material
aplicadas ao modelo usando uma lista de propriedades que afetam vários aspectos da aparência do modelo.

O menu **Materiais** da Exibição 3D permite verificar qual sombreador é usado para cada um dos materiais da cena.

<a name="openpbr"></a>

## OpenPBR

O Designer usa o modelo de material [OpenPBR](https://academysoftwarefoundation.github.io/OpenPBR/) por padrão, que oferece suporte a vários efeitos complexos, como anisotropia,
transmissão e difusão.

Os [modelos de gráfico](../../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md#graph-templates) padrão e as [amostras de material](../../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md#material-samples) incluídas no Designer são todos baseados no modelo de OpenPBR.

As propriedades deste sombreador seguem a [referência de parâmetro de OpenPBR](https://academysoftwarefoundation.github.io/OpenPBR/#parameterreference) e são *compartilhadas* no Rasterizador,
GPU Pathtracer e [renderizadores 3D OpenGL](../3d-renderers/3d-renderers.md).

+++ UVs

| Parâmetro | Tipo | Padrão | Descrição |
|---------------------------------|---------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Revestimento | Float | 1.0 | A quantidade de repetições de textura em uma célula UV, onde um valor mais alto<br/>resulta em mais repetições de textura. |
| Ativar tamanho físico a partir do gráfico | Boolean | Falso | Ajuste automaticamente a divisão em blocos gráficos de acordo com o [Tamanho físico](../../../compositing-graphs/graph-parameters/graph-parameters.md)<br/>do gráfico para representar o material na escala apropriada. |
| Escala UV | Float2 | 1.0, 1.0 | Ajusta a escala da divisão em blocos gráficos por um fator separado para U e V, onde<br/>um valor mais alto resulta em mais repetições de textura. |

+++

+++ Base

| Parâmetro | Tipo | Padrão | Descrição |
|-------------------|--------------|---------------|-------------------------------------------------------------------------------------------------------|
| Peso | Float | 1.0 | Multiplicador da intensidade do reflexo da base difusa e metálica. |
| Cor | Float3 (RGB) | 0.8, 0.8, 0.8 | Cor do reflexo da base difusa e metálica. |
| Metalicidade | Float | 0.0 | Especifica o grau de metalização do material de base. (Alterna a base de dielétrico puro para metal puro) |
| Aspereza difusa | Float | 0.0 | Aspereza do reflexo difuso. Valores mais altos fazem com que a superfície pareça mais plana. |

+++

+++ Especular

| Parâmetro | Tipo | Padrão | Descrição |
|------------|--------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Peso | Float | 1.0 | Multiplica a refletividade especular. |
| Cor | Float3 (RGB) | 1.0, 1.0, 1.0 | Cor do reflexo do specular. (Controla a tonalidade da borda física para metais,<br/>e uma tonalidade geral não física para dielétricos) |
| Aspereza | Float | 0.3 | A aspereza do reflexo do specular. Números mais baixos produzem reflexos mais nítidos<br/>enquanto números mais altos produzem reflexos mais desfocados. |
| Anisotropia | Float | 0.0 | A polarização direcional da aspereza da base metálica/dielétrica, resultando<br/>em realces cada vez mais esticados ao longo da direção tangente. |
| IOR | Float | 1.5 | Índice de refração da base dielétrica. |

+++

+++ Transmissão

| Parâmetro | Tipo | Padrão | Descrição |
|------------------|--------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Peso | Float | 0.0 | Massa da mistura entre a base dielétrica transparente e opaca.<br/>Quanto maior o valor, mais transparente será o material. |
| Cor | Float3 (RGB) | 1.0, 1.0, 1.0 | Controla a cor da base transparente devido à lei de Beer volumétrica<br/>absorção sob a superfície. |
| Profundidade | Float | 0.0 | Especifica a distância em que a luz viaja dentro da base transparente antes de<br/>se tornar exatamente o `transmission_color` de acordo com a lei de Beer. |
| Dispersão | Float3 (RGB) | 0.0, 0.0, 0.0 | Controla a cor da luz dispersa volumetricamente dentro da base transparente. |
| Anisotropia | Float | 0.0 | A quantidade de polarização direcional, ou anisotropia, da dispersão volumétrica<br/>na base transparente. |
| Escala de dispersão | Float | 0.0 | Dimensiona linearmente a quantidade de dispersão. |
| Número Abbe | Float | 20.0 | Número Abbe físico do meio dielétrico, descrevendo quanto<br/>o índice dielétrico de refração varia ao longo dos comprimentos de onda. |

+++

+++ Subsuperfície

| Parâmetro | Tipo | Padrão | Descrição |
|--------------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Peso | Float | 0.0 | Peso da mistura que marca a base dielétrica opaca entre<br/>o reflexo difuso e a dispersão da subsuperfície. |
| Cor | Float3 (RGB) | 0.8, 0.8, 0.8 | A cor de reflexão observada do meio de dispersão subsuperficial. |
| Raio | Float | 1.0 | Escala de comprimento do caminho livre médio da dispersão subsuperficial. |
| Escala do raio | Float3 (RGB) | 1.0, 0.5, 0.25 | multiplicador de RGB para subsurface_radius, fornecendo dispersão por canal<br/>caminhos sem média. |
| Anisotropia | Float | 0.0 | Controla a função de fase da dispersão da subsuperfície, onde zero<br/>dispersão a luz uniformemente, valores positivos dispersões para frente e valores negativos<br/>dispersões para trás. |

+++

+++ Casaco

| Parâmetro | Tipo | Padrão | Descrição |
|------------|--------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Peso | Float | 0.0 | O peso de presença de uma camada refletora de revestimento transparente em cima do material.<br/>Use para materiais como pintura de carro ou camada oleosa. |
| Cor | Float3 (RGB) | 1.0, 1.0, 1.0 | A cor da transparência da camada de verniz transparente, devido à absorção no revestimento. |
| Aspereza | Float | 0.0 | A aspereza das reflexões de camada clara.<br/>Quanto menor o valor, mais nítido será o reflexo. |
| Anisotropia | Float | 0.0 | A polarização direcional da aspereza da camada de camada de camada clara,<br/>resultando em realces cada vez mais esticados ao longo da direção tangente da pelagem. |
| IOR | Float | 1.6 | O índice de refração da camada de verniz transparente. |
| Escurecendo | Float | 1.0 | Modula o efeito de escurecimento físico do pelo. |

+++

+++ Difusão

| Parâmetro | Tipo | Padrão | Descrição |
|-----------|--------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Peso | Float | 1.0 | O peso de presença de uma camada de fuzz que pode ser usada para aproximar microfibras,<br/>para tecidos como veludo e cetim, bem como grãos de dust. |
| Cor | Float3 (RGB) | 1.0, 1.0, 1.0 | A cor da camada difusa. |
| Aspereza | Float | 0.5 | A aspereza da camada difusa. |

+++

+++ Emissão

| Parâmetro | Tipo | Padrão | Descrição |
|-----------|--------------|---------------|------------------------------------------------------|
| Luminância | Float | 0.0 | O valor da luz emitida, expresso como luminância em nits. |
| Cor | Float3 (RGB) | 1.0, 0.0, 0.0 | A cor da luz emitida. |

+++

+++ Filme fino

| Parâmetro | Tipo | Padrão | Descrição |
|-----------|-------|---------|-------------------------------------------------------------------------------------------------------|
| Peso | Float | 0.0 | Peso da cobertura da película fina.<br/>Use para materiais como pintura de carro multitons ou bolhas de sabão. |
| Espessura | Float | 0.5 | O thickness da camada de filme fino na base. (em micrômetros) |
| IOR | Float | 1.4 | O índice de refração do filme fino. |

+++

+++ Geometria

| Parâmetro | Tipo | Padrão | Descrição |
|-------------------|--------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opacidade | Float | 1.0 | A opacidade de todo o material. |
| Parede fina | Boolean | Falso | Se verdadeiro, a superfície é dupla face e representa uma camada infinitamente fina.<br/>Adequado para objetos extremamente geometricamente finos, como folhas ou papel. |
| Normal | Float3 (RGB) | 0.5, 0.5, 1.0 | Insira a normal geométrica para a superfície. |
| Tangente | Float3 (RGB) | 1.0, 0.5, 0.0 | Insira a tangente geométrica. |
| Normal do Revestimento | Float3 (RGB) | 0.5, 0.5, 1.0 | Entrada normal para a camada de revestimento. |
| Tangente do revestimento | Float3 (RGB) | 1.0, 0.5, 0.0 | Insira a tangente geométrica para a camada de revestimento. |
| Altura | Float | 0.5 | Quantidade de deslocamento (ou relevo) na direção do normal.<br/>Quando o height é igual ao nível do height, não há deslocamento.<br/>O Deslocamento é uma alteração escalar na posição da superfície em direção à superfície normal<br/>misturada e não perturbada.<br/>Nos casos em que o deslocamento com mosaico não é possível ou desejado, o height<br/>pode ser implementado como um mapa de relevo. |
| Nível da altura | Float | 0.5 | Valor de height que não corresponde a nenhum deslocamento (valor de nível zero).<br/>O nível de Height desloca (mas não dimensiona nem vira) o deslocamento relativo<br/>à superfície do objeto não deslocado.<br/>Se o nível de height for 0, todo o deslocamento estará acima.<br/>Se o nível de height for 1, todo o deslocamento estará abaixo da superfície, mas ainda manterá<br/>a mesma escala e direção. |
| Escala da altura | Float | 1.0 | Escala de deslocamento ou relevo nas unidades do espaço da cena.<br/>A magnitude e a direção da escala são independentes do valor do nível de height. |
| Oclusão Ambiente | Float | 1.0 | Mapa de oclusão ambiente para escurecer áreas ocultadas.<br/>Branco (1.0) significa totalmente iluminado, preto (0.0) significa totalmente ocultado. |

+++

### Compatibilidade com gráficos existentes

Algumas das propriedades do material de OpenPBR têm identificadores de uso diferentes em comparação com outros modelos incluídos no Designer.
O Designer faz a correspondência automática de alguns identificadores para garantir a compatibilidade com o OpenPBR como modelo padrão.

+++ Mapeamentos de uso herdados para OpenPBR

| Legado | OpenPBR |
|-------------------------|-----------------------------|
| metálico | metalness |
| specularCorAresta | specularColor |
| de aspereza | aspereza especular |
| anisotropyLevel | anisotropiaAsperezaEspecular |
| IOR | specularIOR |
| colorDeabsorção | transmissionColor |
| absorçãoDistância | transmissionDepth |
| translucidez | subsurfaceWeight |
| scatteringColor | subsurfaceColor |
| scatteringDistance | subsurfaceRadius |
| scatteringDistanceScale | subsurfaceRadiusScale |
| coatOpacity | pesoDaPelagem |
| sheenOpacity | fuzzWeight |
| sheenColor | fuzzColor |
| ghenRoughness | fuzzRoughness |
| emissivo | emissionColor |

+++

### Leitura adicional

Para saber mais sobre OpenPBR, aqui estão alguns recursos:

* [artigo do blog do Adobe](https://blog.adobe.com/en/publish/2023/08/08/openpbr-strengthens-interoperability-enabling-enhanced-creativity)
* [White paper](https://academysoftwarefoundation.github.io/OpenPBR/)
* [Adobe OpenPBR BSDF no GitHub](https://github.com/adobe/openpbr-bsdf)
* [Designer 16.0: Suporte de OpenPBR](../../../release-notes/version-16-0/version-16-0.md#openpbr-support)

<a name="adobe-standard-material"></a>

## Material Padrão da Adobe

O modelo Adobe Standard Material (ASM) foi introduzido no Designer 11.2 e foi o sombreador padrão do Designer
até a versão 15.1.

Embora o Designer tenha mudado para OpenPBR como seu novo modelo padrão, o ASM ainda está incluído e suas propriedades também são compartilhadas
no Rasterizador, GPU Pathtracer e nos [renderizadores 3D OpenGL](../3d-renderers/3d-renderers.md).

O modelo está documentado [aqui](https://experienceleague.adobe.com/en/docs/substance-3d/general-knowledge/asm/adobe-standard-material).

<a name="usdpreviewsurface"></a>

## UsdPreviewSurface

A finalidade do modelo UsdPreviewSurface é visualizar materiais com um conjunto de recursos básicos que promova a compatibilidade
entre renderizadores que incluem o USD e/ou a Hydra.

No Designer, este modelo de material só é suportado pelo Rasterizador e pelos [renderizadores 3D](../3d-renderers/3d-renderers.md) de GPU Pathtracer.

O modelo está documentado [aqui](https://openusd.org/dev/spec_usdpreviewsurface.html).
