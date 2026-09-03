---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/3d-renderers.html"
breadcrumb-title: ''
description: Escolha entre os renderizadores rasterizador e pathtracer na visualização 3D para obter diferentes qualidade e desempenho de visualização.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > 3D renderers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderizadores 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1632'
ht-degree: 7%

---


# Renderizadores 3D

A visualização 3D oferece quatro renderizadores:

* Duas versões do renderizador 3D interno Adobe: o Rasterizador para visualização em tempo real com suporte para sombras e o GPU Pathtracer para renderização precisa de sombras, reflexos, propriedades de material complexas e muito mais.
* Dois renderizadores de terceiros obsoletos: OpenGL e NVIDIA&#39;s Iray.

>[!NOTE]
>
> Mantenha os drivers gráficos atualizados!
> 
> Os novos renderizadores 3D são atualizados regularmente e algumas dessas atualizações exigem drivers de GPU recentes. Atualize os drivers de GPU do sistema para a versão mais recente para obter a melhor confiabilidade e suporte dos recursos de renderização.
> 
> Você pode encontrar drivers aqui: [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us) [AMD](https://www.amd.com/en/support) [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

+++ Comparação entre Rasterizador / GPU pathtracer

<table>
  <tr>
    <td>
      <img src="3d-renderers.resources/3d-renderers-01.jpg" alt="3dRendererRasterizer-2">
      <br><i>Rasterizador</i>
    </td>
    <td>
      <img src="3d-renderers.resources/3d-renderers-02.jpg" alt="3dRendererPathtracer-2">
      <br><i>GPU Pathtracer</i>
    </td>
  </tr>
</table>

+++

O renderizador Adobe 3D foi criado inteiramente para suportar tecnologias modernas, como a linguagem de sombreamento [MaterialX](https://materialx.org/) e a descrição de cena do [USD](https://openusd.org/release/index.html), e está pronto para oferecer consistência visual total em todo o ecossistema Substance 3D.

Graças à sua dependência do USD, ele pode aproveitar o [plug-in USDFileFormat](https://github.com/adobe/USD-Fileformat-plugins) do Adobe para importar muitos formatos de cena 3D, como FBX e GLTF, e renderizar essas cenas completamente, incluindo materiais, texturas, câmeras e luzes.

+++ Importação de cena: Rasterizador vs. OpenGL

<table>
  <tr>
    <td>
      <img src="3d-renderers.resources/3d-renderers-01.jpg" alt="3dRendererRasterizer-2">
      <br><i>Rasterizador</i>
    </td>
    <td>
      <img src="3d-renderers.resources/3d-renderers-03.jpg" alt="3dRendererOpenGL-2">
      <br><i>OpenGL</i>
    </td>
  </tr>
</table>

+++

>[!TIP]
>
> Você pode selecionar o renderizador usado por padrão ao iniciar uma nova Visualização 3D na seção [”Exibição 3D” das configurações do projeto](../../../interface/preferences-window/project-settings/project-settings.md).

<a name="rasterizer"></a>

## Conversor de Bitmap

+++ Parâmetros

|                                                                 |                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Amostras** Precisão decimal | Especifica o número de amostras de pixels a serem computadas antes que a imagem seja considerada convergida. |
| Precisão decimal de **opacidade de Oclusão de ambiente** | Especifica o valor da opacidade da oclusão do ambiente. |
| **Habilitar deslocamento** Booleano | Especifica se o deslocamento deve ser habilitado. |
| **Precisão decimal de limite de Deslocamento** | Configura um limite para habilitar/desabilitar a tesselação da GPU. |
| **Habilitar remoção de face de fundo** booleano | Um valor verdadeiro permitirá a remoção de malhas triangulares que têm normais que estão voltadas para longe da câmera. Um valor false desabilitará a remoção de face de fundo. |
| **Modo de diagnóstico** Inteiro | Determina o modo de diagnóstico a ser renderizado. |
| **Modo de sombra do rasterizador** Inteiro | Especifica a técnica a ser usada para renderizar sombras:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Nenhuma sombra:</i> nenhuma sombra será renderizada.</li> <li data-preserve-html="true"><i>Voxel marchou:</i> marche os raios de sombra em uma cena voxelizada.</li> </ul> |
| **Contagem de amostra de sombra do rasterizador** Inteiro | Especifica quantos raios de sombra são traçados por pixel. |
| **Precisão decimal de opacidade de sombra do rasterizador** | Especifica a opacidade das sombras, de 0,0 (sem sombras) a 1,0 (sombras completas). |
| **Transparência independente de ordem do rasterizador habilitada** Booleano | Não considera a ordem das superfícies transparentes ao renderizá-las. Isso sacrifica um pouco a precisão para uma renderização mais rápida de superfícies transparentes. |
| **Habilitar SSS de rasterizador** Booleano | Alterna o efeito de dispersão da subsuperfície. |
| **Contagem de exemplo de SSS de rasterizador** Inteiro | Especifica quantas amostras são tiradas por pixel para renderizar a dispersão da subsuperfície. |
| **Habilitar suavização de contornos de acúmulo de rasterizador** booliano | Alterna a suavização de contornos de acumulação, que melhora o smoothness ou as bordas da imagem renderizada por renderizações irregulares e pelo cálculo da cor média local de cada pixel, cumulativamente. Ou seja, ele acumula valores para calcular uma média. |
| **Resolução da grade de voxels rasterizada** Inteiro | Determina a resolução da grade de voxel usada em voxel que marca o rasterizador.   Valores mais altos resultam em sombras mais precisas em detrimento do desempenho. |
| **Contagem de exemplo de tempo de execução de IBL de rasterizador** Inteiro | Especifica quantas amostras são usadas para calcular os reflexos de specular de IBL quando a técnica está definida como `runtimeSampled`. |

+++

+++ Plano do solo

|                               |                                                                                                                                                              |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Booleano **Habilitado** | Alterna o plano do solo na cena renderizada. |
| **Height** flutuante | Controla o deslocamento do height do plano do solo.   Se for criado, espera-se que o valor tenha a polarização apropriada inserida, com base na escala da cena. |
| **Intensidade da sombra** flutuante | Quando as sombras estão ativadas, controla a opacidade das sombras projetadas no plano do solo, de 0,0 (sem sombras) a 1,0 (sombras completas). |

+++

![Rasterizador - Exemplo 1](3d-renderers.resources/3d-renderers-04.jpg "Rasterizador - Exemplo 1"){zoomable="yes"}

<a name="gpu-pathtracer"></a>

## Rastreador de caminho da GPU

+++ Parâmetros

|                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Amostras** Precisão decimal | Especifica o número de amostras de pixels a serem computadas antes que a imagem seja considerada convergida. |
| **Habilitar deslocamento** Booleano | Especifica se o deslocamento deve ser habilitado. |
| **Precisão decimal de limite de Deslocamento** | Configura um limite para habilitar/desabilitar a tesselação da GPU. |
| **Habilitar remoção de face de fundo** booleano | Um valor verdadeiro permitirá a remoção de malhas triangulares que têm normais que estão voltadas para longe da câmera. Um valor false desabilitará a remoção de face de fundo. |
| **Tipo de ciclo de pixels** Inteiro | Especifica a técnica a ser usada para diminuir a resolução de computação para renderização interativa:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Sem ciclo:</i> desabilita o ciclo de pixels e computa cada amostra de pixel completa.</li> <li data-preserve-html="true"><i>Ideal para dispositivos:</i> seleciona a resolução de ciclos de pixel ideal com base no dispositivo usado para renderização.</li> <li data-preserve-html="true"><i>4x4:</i> Amostra 1/16 dos pixels por passagem de ciclo.</li> <li data-preserve-html="true"><i>8x8:</i> Amostra 1/64 dos pixels por passagem de ciclo.</li><li data-preserve-html="true"><i>Ruído azul:</i> faz a amostragem adaptativamente de um número de pixels e os divide para atingir uma taxa de quadros de objetivo.</li> </ul> |
| **Modo de diagnóstico** Inteiro | Determina o modo de diagnóstico a ser renderizado. |
| **Exibir plano de fundo através da transmissão** Booleano | Um valor verdadeiro permite que a imagem de fundo seja vista através de objetos transmissivos ou refrativos.   Quando for falso, objetos transmissivos mostrarão a imagem refratada do ambiente da cena. |

+++

+++ Plano do solo

|                                    |                                                                                                                                                                  |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Booleano **Habilitado** | Alterna o plano do solo na cena renderizada. |
| **Height** flutuante | Controla o deslocamento do height do plano do solo.   Se for criado, espera-se que o valor tenha a polarização apropriada inserida, com base na escala da cena. |
| **Intensidade da sombra** flutuante | Quando as sombras estão ativadas, controla a opacidade das sombras projetadas no plano do solo, de 0,0 (sem sombras) a 1,0 (sombras completas). |
| **Habilitar luzes locais** booleano | Controla se a iluminação direta das luzes locais contribui para os detectores de sombra. |
| **Habilitar reflexos** booleano | Controla a visibilidade de todos os reflexos no plano do solo. |
| **Opacidade dos reflexos** flutuante | Quando os reflexos estão ativados, controla a opacidade dos reflexos, entre 0,0 (nenhum reflexo) e 1,0 (reflexos completos). |
| **Aspereza de reflexos** flutuante | Quando os reflexos estão ativados, controla a aspereza do material do plano do solo que contribui para os reflexos, de 0,0 (totalmente brilhante) a 1,0 (totalmente áspero). |

+++

![GPU pathtracer - Exemplo 1](3d-renderers.resources/3d-renderers-05.jpg "GPU pathtracer - Exemplo 1"){zoomable="yes"}

<a name="opengl"></a>

## OpenGL

O renderizador OpenGL oferece renderização rápida em tempo real, com alguns sombreadores disponíveis por padrão, dependendo do caso de uso: consulte a lista abaixo.

+++ OpenPBR

Um modelo de material com suporte crescente apoiado pelos principais atores do setor, inclusive o Adobe, e com o mais amplo conjunto de recursos.

Duas técnicas estão disponíveis para visualizar o height:

<b>Oclusão de paralaxe</b> - Falsa deslocamento de height sem modificar a geometria por meio de deformação UV localizada e oclusão.

<b>Tesselação + Deslocamento</b> - Subdivide a geometria e desloca os vértices ao longo de suas normais.

Saiba mais sobre OpenPBR no Designer [aqui](../material-properties/material-properties.md#openpbr).

+++


+++ Material Padrão da Adobe

Adobe padronizou o sombreador. Garante aparência correta entre todos os aplicativos Adobe Substance 3D e suporta um amplo conjunto de recursos.

Duas técnicas estão disponíveis para visualizar o height:

<b>Oclusão de paralaxe</b> - Falsa deslocamento de height sem modificar a geometria por meio de deformação UV localizada e oclusão.

<b>Tesselação + Deslocamento</b> - Subdivide a geometria e desloca os vértices ao longo de suas normais.

O Material Padrão da Adobe está documentado em detalhes nesta [seção](https://experienceleague.adobe.com/en/docs/substance-3d/general-knowledge/asm/adobe-standard-material) de nossa documentação.

+++

+++ AxF SVBRDF

Um sombreador dedicado para visualizar materiais extraídos de arquivos [AxF](../../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) e usando a representação <b>SVBRDF</b>.

Duas técnicas estão disponíveis para visualizar o height:

<b>Oclusão de paralaxe</b> - Falsa deslocamento de height sem modificar a geometria por meio de deformação UV localizada e oclusão.

<b>Tesselação + Deslocamento</b> - Subdivide a geometria e desloca os vértices ao longo de suas normais.

Este sombreador é atualmente um *trabalho em andamento* e fornece uma visão geral das características dos materiais, mas não deve ser usado para ajustes finos, e alguns recursos ainda não são suportados.

+++

+++ Blinn

“Antiga - geração”, sombreador correto não PBR. Usa os canais Difuso, Specular e Textura reluzente ao lado dos canais padrão como Opacidade, Height e Normal.

Duas técnicas estão disponíveis para visualizar o height:

<b>Oclusão de paralaxe</b> - Falsa deslocamento de height sem modificar a geometria por meio de deformação UV localizada e oclusão.

<b>Tesselação + Deslocamento</b> - Subdivide a geometria e desloca os vértices ao longo de suas normais.

+++

+++ Lambert

Sombreador de iluminação lambert muito simples, só oferece suporte para canal Difuso. Usa o antigo sistema de luzes de ponto, não é compatível com iluminação de imagem HDR.

+++

+++ Informações da malha

Depurar sombreador não iluminado para visualizar os seguintes dados de geometria:

* Normal

* Tangente

* Binormal

* UV

* Bloco UV

* Cor do vértice

* Posição (espaço global)

A visualização é fixada a [0, 1]. Por conseguinte, não é possível obter uma leitura direta de valores fora desse intervalo no ecrã.

+++

+++ Aspereza metálica

Material PBR padrão para o modelo Aspereza metálica. Usa os canais de Cor base, Metálico e Aspereza.

Duas técnicas estão disponíveis para visualizar o height:

<b>Oclusão de paralaxe</b> - Falsa deslocamento de height sem modificar a geometria por meio de deformação UV localizada e oclusão.

<b>Tesselação + Deslocamento</b> - Subdivide a geometria e desloca os vértices ao longo de suas normais.

+++

+++ Aspereza metálica - Revestida

Material PBR revestido para o modelo Aspereza metálica. Usa cor base, canais metálicos e de aspereza, bem como canais extras de “Revestimento”.

Duas técnicas estão disponíveis para visualizar o height:

<b>Oclusão de paralaxe</b> - Falsa deslocamento de height sem modificar a geometria por meio de deformação UV localizada e oclusão.

<b>Tesselação + Deslocamento</b> - Subdivide a geometria e desloca os vértices ao longo de suas normais.

+++

+++ Aspereza metálica - SSS

Material PBR de dispersão de subsuperfície para o modelo Aspereza metálica. Usa cor base, canais Metálicos e de Aspereza, bem como canal de Dispersão extra.

Duas técnicas estão disponíveis para visualizar o height:

<b>Oclusão de paralaxe</b> - Falsa deslocamento de height sem modificar a geometria por meio de deformação UV localizada e oclusão.

<b>Tesselação + Deslocamento</b> - Subdivide a geometria e desloca os vértices ao longo de suas normais.

+++

+++ brilho do specular

Material PBR padrão para o modelo de brilho de Specular. Usa canais Difusos, de Specular e Textura reluzente.

Duas técnicas estão disponíveis para visualizar o height:

<b>Oclusão de paralaxe</b> - Falsa deslocamento de height sem modificar a geometria por meio de deformação UV localizada e oclusão.

<b>Tesselação + Deslocamento</b> - Subdivide a geometria e desloca os vértices ao longo de suas normais.

+++

+++ Desativado

Sombreador de depuração não iluminado para visualizar mapas de textura sem qualquer iluminação. Usa apenas um canal &#39;color&#39;.

+++

O Designer também oferece a possibilidade de configurar seus próprios sombreadores para o renderizador OpenGL [usando arquivos GLSLFX](../../../interface/3d-view/glslfx-shaders/glslfx-shaders.md).

>[!IMPORTANT]
> 
> Este renderizador está **obsoleto**: ele não receberá novos recursos e será desativado em uma versão futura do Designer.

![OpenGL - Exemplo 1](3d-renderers.resources/3d-renderers-06.jpg "OpenGL - Exemplo 1"){zoomable="yes"}
