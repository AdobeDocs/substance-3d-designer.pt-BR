---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render.html"
breadcrumb-title: ''
description: Use o nó Renderização PBR para renderizar materiais baseados fisicamente com iluminação realista para visualizar a aparência do material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderização PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 1%

---


# Renderização PBR

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render.png){width="250px"}

**Entrada:** *Filtros de Material/Utilitários PBR*

**Complexo**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

Renderiza um material PBR em uma esfera, plano ou cilindro usando Iluminação baseada em imagem (IBL). Este é um mecanismo de renderização dentro de um nó, que pode ser muito útil para gerar miniaturas, visualizações ou ativos 2D. Não é um renderizador como a visualização 3D, mas uma textura real sendo gerada no seu gráfico.

Este nó requer pelo menos um material PBR completo para ser conectado. Idealmente, você deve usar os modos de criação de link para conectar o material à Renderização PBR. Além disso, você precisará de um ambiente HDRI esfericamente desempacotado para que a renderização calcule a iluminação de onde. Os materiais para teste podem ser encontrados em Materiais PBR, Mapas de ambiente podem ser encontrados em [Exibição 3D na biblioteca.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/3d-view-library.md)

</td>
</tr>
</table>

>[!WARNING]
>
> **Mecanismo da CPU (SSE2)**
> 
> O nó Renderização PBR é muito pesado e não funciona bem com o mecanismo de CPU SSE2. Alterne para outro mecanismo pressionando F9, se o nó tiver um desempenho extremamente ruim.

## Entradas

* **Canal de material** **entradas**\
  Várias entradas de material são usadas para renderizar o material na geometria:
  * Cor de base
  * Normal
  * Emissivo
  * Aspereza
  * Metálico
  * Nível especular
  * Altura
  * Oclusão de ambiente
  * Máscara de opacidade
  * Nível de anisotropia
  * Ângulo de anisotropia
  * Translucidez
  * Escala de distância de dispersão
* **Mapa de Dirt de lente**: *Entrada em tons de cinza* Mapa personalizado para dirt na lente, que aparece quando reflexos de lente são visíveis.
* **Mapa de Abertura da Lente**: a *Entrada em Tons de Cinza* pode ser usada para substituir a forma Bokeh fora de foco. Quanto mais contrastada, mais visível ela será. Lembre-se de que apenas um círculo na textura é amostrado, portanto qualquer forma deve caber dentro de um círculo.
* **Entrada do plano de fundo**: *Entrada de cores*\
  Mapa personalizado usado como plano de fundo quando o parâmetro **Modo de Plano de Fundo** está definido como *Entrada de Plano de Fundo*
* **Mapa de ambiente**: *Entrada de cores* mapa de ambiente usado para calcular a iluminação. Deve ser mapeado esfericamente e em HDR

Saídas

* **Beleza**\
  A renderização final
* **Irradiância bruta**\
  Os dados de irradiância do processamento final\
  *Alpha:* mapa de opacidade
* **Specular bruto**\
  Os dados de specular da renderização final\
  *Alpha:* mapa de sombras de Specular
* **Espaço Mundial Normal**\
  Os dados normais do espaço global da renderização final\
  *Alpha:* mapa do height do espaço global
* **Espaço Tangente Normal**\
  Os dados normais do espaço tangente da renderização final\
  *Alpha:* mapa de height de espaço tangente
* **UVs**\
  Os dados UV da renderização final\
  *Alpha:* mapa de opacidade

## Parâmetros

* **Forma**: *Esfera, Plano, Cilindro*\
  Define a forma usada para renderização. Formas personalizadas não são possíveis.
* **Intensidade do Deslocamento**: *0.0 - 0.5* Defina a intensidade do deslocamento a partir do height.
* **Rotação do Ambiente**: *0.0 - 1.0*\
  Gira o ambiente de iluminação. Gira previamente em comparação com a movimentação da câmera.
* **Modo Em Segundo Plano**: *Cor, Ambiente, Ambiente, Entrada Em Segundo Plano*\
  Defina o que é mostrado em segundo plano. Cor é uma cor sólida, Ambiente é o mapa que você conectou com um desfoque opcional. Ambiente é uma versão muito desfocada do ambiente.
* **Cor do plano de fundo**: *(Valor da cor)*\
  Disponível somente quando o modo Plano de fundo está definido como Cor.
* **Desfoque do Plano de Fundo do Ambiente**: *0.0 - 1.0*\
  Disponível somente quando o modo Segundo plano estiver definido como Ambiente.
* **Forma**
  * **Escala**: *0.0 - 2.0*\
    Defina a escala da esfera.
  * **Tamanho do Plano**: *0.0 - 1.0*\
    Defina a escala para o plano.
  * **Raio do cilindro**: *0.0 - 1.0*\
    Defina o raio do cilindro.
  * **Comprimento do Cilindro**: *0.0 - 1.0*\
    Defina o comprimento do cilindro.
  * **Rotação**: *0.0 - 1.0*\
    Gira a forma sem girar a iluminação.
  * **Direção da Rotação**: *0.0 - 1.0*\
    Define o eixo de rotação em 2D.
  * **Rotação em torno da Direção**: *0.0 - 1.0*\
    Gira a forma no eixo de rotação.
  * **Posição da Forma**: *-1.0 - 1.0*\
    Move formas.
  * **Divisão em blocos gráficos UV**: *1.0 - 6.0*\
    Define a quantidade de UV-Tiling.
  * **Escala UV de esfera**: *0.0 - 4.0*\
    Define a escala dos UVs na esfera.
  * **Escala UV de plano**: *1.0 - 4.0*\
    Define a escala dos UVs no plano.
  * **Escala UV do cilindro**: *1.0 - 6.0*\
    Define a escala dos UVs no Cilindro.
  * **Deslocamento UV**: *0.0 - 1.0*\
    Compensa UVs
  * **UVs de inclinação**: *Falso/Verdadeiro*\
    Inclina os UVs em 45 graus para a esfera.
* **Câmera**
  * **Exposição**: *-4.0 - 4.0*\
    Defina a exposição da câmera.
  * **Mapeador de tons**: *Linear, ACES, Hejl cinematográfico*\
    Defina a solução de mapeamento de tom a ser usada para a imagem final.
  * **Modo de Câmera**: *Perspectiva, Ortográfico*\
    Alterne a câmera entre dois modos de projeção.
  * **Campo de Exibição**: *0.01 - 100.0*\
    Definir ângulo CDV da câmera.
  * **Distância**: *0.0 - 4.0*\
    Defina a distância da câmera do centro do objeto.
  * **Intensidade da vinheta**: *0.0 - 1.0*\
    Defina a intensidade do efeito de vinheta.
  * **Raio da vinheta**: *0.0 - 1.0*\
    Defina o raio do efeito de vinheta.
  * **Posição da Tela**:\
    Move a câmera ao redor do objeto. Também é possível alterar um gizmo na exibição 2D.
* **Profundidade de campo**
  * **Raio de abertura** : *0.0 - 0.1* Define o raio da abertura. Valores mais altos significam que as áreas fora de foco ficam mais desfocadas (bokeh).
  * **Lâminas De Abertura**: *3 - 9*\
    Define a forma do desfoque bokeh.
  * **Anel de Abertura**: *0.0 - 1.0*\
    Adiciona um gradiente interno à forma bokeh.
  * **Difração de abertura**: *0.0 - 2.0*\
    Adiciona desvio cromático ao bokeh.
  * **Bokeh Irregular**: *0.0 - 1.0*\
    Adiciona um efeito de giro ou giro às áreas de desfoque bokeh fora de foco.
  * **Modo de Foco**: *Automático, Ponto*\
    Defina se o foco é predeterminado ou definido pelo usuário. O foco de ponto permite mover um ponto na exibição 2D para determinar a distância de foco.
  * **Ponto de Foco**:\
    Se o foco estiver definido como Ponto, você poderá mover esse ponto. tem um gizmo de exibição 2D.
  * **Deslocamento de Foco**: *-0.5 - 0.5*\
    Se o foco estiver definido como Automático, você poderá deslocá-lo para frente e para trás.
  * **Usar o Mapa de Abertura Personalizado**: *Falso/Verdadeiro*\
    Substitui as configurações de Abertura acima e usa a entrada do mapa de Abertura para determinar a forma do bokeh. Requer uma entrada.
* **Pós-efeitos**
  * **Habilitar Pós-Efeitos**: *Falso/Verdadeiro*\
    Alterna *todos* os pós-efeitos na renderização final.
  * **Intensidade de desabrochar** : *0.0 - 2.0* Define a intensidade do efeito de desabrochar.
  * **Limite de Bloom** : *0.0 - 2.0* Define o limite baixo para que o bloom apareça.
  * **Bloom Chroma Shift** : *0.0 - 1.0*
  * **Intensidade de halo da lente** : *0.0 - 1.0* Define a intensidade do efeito de halo da lente.
  * **Intensidade de Clarões de Lente** : *0.0 - 1.0* Define a intensidade do clarão de lente. Certifique-se de que a luz do plano de fundo do ambiente esteja visível para ver corretamente esse efeito.
  * **Intensidade do Dirt de lente** : *0.0 - 1.0* Define o efeito do mapa de dirt de lente nos reflexos da lente.
* **Configurações de renderização**
  * **Qualidade Difusa**: *16 Amostras, 32 Amostras, 64 Amostras, 128 Amostras*\
    Alternar entre os níveis de qualidade do mapa difuso.
  * **Multiplicador Emissivo Difuso**: *0.0 - 1.0*\
    Controla o quanto as partes emissivas estão contribuindo para a irradiância.
  * **Intensidade de sombra difusa**: *0.0 - 1.0*\
    Controla a intensidade das sombras difusas.
  * **Pontilhamento de Specular**: *0.0 - 1.0*\
    Defina a intensidade de pontilhamento do specular.
  * **Multiplicador de Sombra do Specular**: *0.0 - 1.0*\
    Controla a intensidade das sombras nos reflexos do specular.
  * **Modo de Opacidade** *Teste de Alpha pontilhado, Mesclagem de Alpha simples*\
    Controla o método de aplicação da transparência. O modo *Mesclagem de Alpha simples* é mais visível em planos de fundo uniformes.
  * **Intensidade de Oclusão do ambiente**: *0.0 - 1.0*\
    Define a intensidade das sombras de oclusão ambiente.
* **Ajustes de material**
  * **Recalcular Normas**: *Falso/Verdadeiro*\
    Os valores normais serão recalculados a partir do mapa de heights de acordo com a intensidade do deslocamento.
  * **Formato Normal**: *DirectX, OpenGL*\
    Alternar entre Formatos de mapa normais diferentes (inverte o canal verde)
  * **Entrada F0 Dielétrica**: *Valor Constante, entrada de Specular level*\
    Defina quais unidades os valores F0. Entrada de specular level significa que será orientada por um mapa de entrada.
  * **Dielétrico F0**: *0.0 - 0.08*\
    Se Valor constante for escolhido para Entrada dielétrica F0, este controle deslizante permite definir o valor global.
* **Limpar revestimento**
  * **Habilitar Revestimento Simples**: *Falso/Verdadeiro*\
    Habilita uma camada de revestimento transparente adicional e simples na parte superior do material de entrada.
  * **Limpar Espessura Da Pelagem**: *0.0 - 1.0*\
    Define a intensidade ou a intensidade da camada de revestimento transparente.
  * **Limpar Specular level de Revestimento**: *0.0 - 1.0*\
    Define a aspereza da camada de revestimento transparente.
  * **Herdar normal da camada base**: *Falso/Verdadeiro* Defina se o clareamento ignorar ou usar normais do material de base.
* **Emissivo**
  * **Habilitar Iluminação Emissiva** *Verdadeiro/Falso* Alterna a contribuição difusa da iluminação emissiva.
  * **Intensidade Emissiva**: *0.0 - 10.0*\
    Define o multiplicador global para o mapa emissivo.
* **Dispersão da Subsuperfície**
  * **Habilitar Dispersão da Subsuperfície** *Verdadeiro/Falso*\
    Alterna a dispersão da subsuperfície na renderização final.\
    *Observação:* a dispersão da subsuperfície requer que o valor de entrada de **Translucidez** seja *maior que 0,0*
  * **Distância de dispersão** *0.0 - 1.0*\
    Ajusta a distância máxima do efeito de dispersão.\
    *Observação:* este valor é multiplicado pelo valor de entrada *por canal de cor* da **Escala de distância de dispersão**.
  * **Turno Vermelho** *0.0 - 1.0*\
    Ajusta a intensidade do efeito Deslocamento de vermelho na dispersão.
  * **Rayleigh** *0.0 - 1.0*\
    Ajusta a intensidade do efeito Rayleigh na dispersão.

## Imagens de exemplo

Todas as imagens foram geradas diretamente dentro do Designer, na viewport 2D, usando materiais da biblioteca [ativos do Substance 3D](https://helpx.adobe.com/substance-3d/unlisted/assets.html).

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/pbr-render-v2.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/sphere-thermal-insulation-panel.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/sphere-ominous-obsidian.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/sphere-forest-gravel-1.jpg" width="300px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c0_image" src="../../../../../../assets/sphere-chesterfield-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_image" src="../../../../../../assets/sphere-carbon-fiber.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c2_image" src="../../../../../../assets/plane-inclined-lumber-tiles.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c3_image" src="../../../../../../assets/cylinder-medieval-leaded-glass-window.jpg" width="300px"/></div> |
|  |  |  |  |
