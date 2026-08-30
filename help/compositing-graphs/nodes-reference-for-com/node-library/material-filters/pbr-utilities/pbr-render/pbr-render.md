---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 6%

---


# Renderização PBR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-render.resources/pbr-render.png){width="250px"}

<b>Entrada:</b> Filtros Materiais > Utilitários PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

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

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entradas de canal de material</b> | Várias entradas de material são usadas para renderizar o material na geometria: <br><br>- Cor de base<br>- Normal<br>- Emissivo<br>- Aspereza<br>- Metálico<br>- Specular level<br>- Height<br>- Oclusão de ambiente<br>- Máscara de Opacidade<br>- Nível de anisotropia<br>- Ângulo de anisotropia<br>- Translucidez<br>- Escala de Distância de Dispersão |
| <b>Mapa de Dirt de lente</b> <i>Entrada em tons de cinza</i> | Mapa personalizado para dirt na lente, que aparece quando reflexos da lente são visíveis. |
| <b>Mapa de abertura da lente</b> <i>Entrada em tons de cinza</i> | Pode ser usado para substituir a forma fora de foco do Bokeh. Quanto mais contrastada, mais visível ela será. Lembre-se de que apenas um círculo na textura é amostrado, portanto qualquer forma deve caber dentro de um círculo. |
| <b>Entrada em segundo plano</b> <i>Entrada de cores</i> | Mapa personalizado usado como plano de fundo quando o parâmetro <b>Modo de Plano de Fundo</b> está definido como <i>Entrada de Plano de Fundo</i> |
| <b>Mapa do ambiente</b> <i>Entrada de cores</i> | Mapa de ambiente usado para calcular a iluminação. Deve ser mapeado esfericamente e em HDR |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Beleza</b> | A renderização final |
| <b>Irradiância bruta</b> | Os dados de irradiância do mapa de opacidade final de renderização<br><br><i>Alpha:</i> |
| <b>Specular bruto</b> | Os dados de specular da renderização final<br><br><i>Alpha:</i> mapa de sombras de Specular |
| <b>Espaço Mundial Normal</b> | Os dados normais do espaço global do renderizador final<br><br><i>Alpha:</i> mapa de altura do espaço global |
| <b>Espaço Tangente Normal</b> | Os dados normais de espaço tangente do mapa de altura do espaço tangente final<br><br><i>Alpha:</i> |
| <b>UVs</b> | Os dados UV do mapa de opacidade final de renderização<br><br><i>Alpha:</i> |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Forma</b> <i>Esfera, Plano, Cilindro</i> | Define a forma usada para renderização. Formas personalizadas não são possíveis. |
| <b>Intensidade de Deslocamento</b> <i>0.0 - 0.5</i> | Defina a intensidade do deslocamento a partir do height. |
| <b>Rotação do ambiente</b> <i>0.0 - 1.0</i> | Gira o ambiente de iluminação. Gira previamente em comparação com a movimentação da câmera. |
| <b>Modo de Tela de Fundo</b> <i>Cores, Ambiente, Ambiente, Entrada de Plano de Fundo</i> | Defina o que é mostrado em segundo plano. Cor é uma cor sólida, Ambiente é o mapa que você conectou com um desfoque opcional. Ambiente é uma versão muito desfocada do ambiente. |
| <b>Cor do plano de fundo</b> <i>(Valor da cor)</i> | Disponível somente quando o modo Plano de fundo está definido como Cor. |
| <b>Desfoque de fundo do ambiente</b> <i>0.0 - 1.0</i> | Disponível somente quando o modo Segundo plano estiver definido como Ambiente. |
| <b>Forma</b> |  |
| <b>Escala</b> <i>0.0 - 2.0</i> | Defina a escala da esfera. |
| <b>Tamanho do plano</b> <i>0.0 - 1.0</i> | Defina a escala para o plano. |
| <b>Raio do cilindro</b> <i>0.0 - 1.0</i> | Defina o raio do cilindro. |
| <b>Comprimento do Cilindro</b> <i>0.0 - 1.0</i> | Defina o comprimento do cilindro. |
| <b>Rotação</b> <i>0.0 - 1.0</i> | Gira a forma sem girar a iluminação. |
| <b>Direção da Rotação</b> <i>0.0 - 1.0</i> | Define o eixo de rotação em 2D. |
| <b>Rotação em torno da direção</b> <i>0.0 - 1.0</i> | Gira a forma no eixo de rotação. |
| <b>Posição da Forma</b> <i>-1.0 - 1.0</i> | Move formas. |
| <b>Divisão em blocos gráficos UV</b> <i>1.0 - 6.0</i> | Define a quantidade de UV-Tiling. |
| <b>Escala UV de esfera</b> <i>0.0 - 4.0</i> | Define a escala dos UVs na esfera. |
| <b>Escala UV de plano</b> <i>1.0 - 4.0</i> | Define a escala dos UVs no plano. |
| <b>Escala UV do cilindro</b> <i>1.0 - 6.0</i> | Define a escala dos UVs no Cilindro. |
| <b>Deslocamento UV</b> <i>0.0 - 1.0</i> | Compensa UVs |
| <b>UVs de inclinação</b> <i>Falso/Verdadeiro</i> | Inclina os UVs em 45 graus para a esfera. |
| <b>Câmera</b> |  |
| <b>Exposição</b> <i>-4.0 - 4.0</i> | Defina a exposição da câmera. |
| <b>Mapeador de tons</b> <i>Hejl Filmômico, ACE</i> | Defina a solução de mapeamento de tom a ser usada para a imagem final. |
| <b>Modo de Câmera</b> <i>Perspectiva, Ortográfica</i> | Alterne a câmera entre dois modos de projeção. |
| <b>Campo de Exibição</b> <i>0.01 - 100.0</i> | Definir ângulo CDV da câmera. |
| <b>Distância</b> <i>0.0 - 4.0</i> | Defina a distância da câmera do centro do objeto. |
| <b>Intensidade da vinheta</b> <i>0.0 - 1.0</i> | Defina a intensidade do efeito de vinheta. |
| <b>Raio da vinheta</b> <i>0.0 - 1.0</i> | Defina o raio do efeito de vinheta. |
| <b>Posição da Tela</b> | Move a câmera ao redor do objeto. Também é possível alterar um gizmo na exibição 2D. |
| <b>Profundidade de campo</b> |  |
| <b>Raio de abertura</b> <i>0.0 - 0.1</i> | Define o raio da abertura. Valores mais altos significam que as áreas fora de foco ficam mais desfocadas (bokeh). |
| <b>Lâminas de abertura</b> <i>3 - 9</i> | Define a forma do desfoque bokeh. |
| <b>Anel de abertura</b> <i>0.0 - 1.0</i> | Adiciona um gradiente interno à forma bokeh. |
| <b>Difração de abertura</b> <i>0.0 - 2.0</i> | Adiciona desvio cromático ao bokeh. |
| <b>Bokeh rodopiado</b> <i>0.0 - 1.0</i> | Adiciona um efeito de giro ou giro às áreas de desfoque bokeh fora de foco. |
| <b>Modo de Foco</b> <i>Automático, Ponto</i> | Defina se o foco é predeterminado ou definido pelo usuário. O foco de ponto permite mover um ponto na exibição 2D para determinar a distância de foco. |
| <b>Ponto de Foco</b> | Se o foco estiver definido como Ponto, você poderá mover esse ponto. tem um gizmo de exibição 2D. |
| <b>Deslocamento de foco</b> <i>-0.5 - 0.5</i> | Se o foco estiver definido como Automático, você poderá deslocá-lo para frente e para trás. |
| <b>Usar o Mapa de Abertura Personalizado</b> <i>Falso/Verdadeiro</i> | Substitui as configurações de Abertura acima e usa a entrada do mapa de Abertura para determinar a forma do bokeh. Requer uma entrada. |
| <b>Pós-efeitos</b> |  |
| <b>Habilitar Pós-efeitos</b> <i>Falso/Verdadeiro</i> | Alterna <i>todos</i> os pós-efeitos na renderização final. |
| <b>Intensidade de Bloom</b> <i>0.0 - 2.0</i> | Define a intensidade do efeito de desabrochar. |
| <b>Limite de Bloom</b> <i>0.0 - 2.0</i> | Define o limite inferior para que o bloom seja exibido. |
| <b>Bloom Chroma Shift</b> <i>0.0 - 1.0</i> |  |
| <b>Intensidade de halo da lente</b> <i>0.0 - 1.0</i> | Define a intensidade do efeito de halo da lente. |
| <b>Intensidade de clarões da lente</b> <i>0.0 - 1.0</i> | Define a intensidade do reflexo de flash. Certifique-se de que a luz do plano de fundo do ambiente esteja visível para ver corretamente esse efeito. |
| <b>Intensidade do Dirt da lente</b> <i>0.0 - 1.0</i> | Define o efeito do mapa de dirt de lente nos reflexos de lente. |
| <b>Configurações de renderização</b> |  |
| <b>Qualidade da Difusão</b> <i>16 Amostras, 32 Amostras, 64 Amostras, 128 Amostras</i> | Alternar entre os níveis de qualidade do mapa difuso. |
| <b>Multiplicador de Emissivo de Difusão</b> <i>0.0 - 1.0</i> | Controla o quanto as partes emissivas estão contribuindo para a irradiância. |
| <b>Intensidade de Sombra da Difusão</b> <i>0.0 - 1.0</i> | Controla a intensidade das sombras difusas. |
| <b>Pontilhamento de Specular</b> <i>0.0 - 1.0</i> | Defina a intensidade de pontilhamento do specular. |
| <b>Multiplicador de Sombra do Specular</b> <i>0.0 - 1.0</i> | Controla a intensidade das sombras nos reflexos do specular. |
| <b>Modo de Opacidade</b> <i>Teste de Alpha pontilhado, Combinar de Alpha simples</i> | Controla o método de aplicação da transparência. O modo <i>Mesclagem de Alpha simples</i> é mais visível em planos de fundo uniformes. |
| <b>Intensidade de Oclusão de ambiente</b> <i>0.0 - 1.0</i> | Define a intensidade das sombras de oclusão ambiente. |
| <b>Ajustes de material</b> |  |
| <b>Recalcular Normas</b> <i>Falso/Verdadeiro</i> | Os valores normais serão recalculados a partir do mapa de heights de acordo com a intensidade do deslocamento. |
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alternar entre Formatos de mapa normais diferentes (inverte o canal verde) |
| <b>Entrada F0 Dielétrica</b> <i>Valor Constante, entrada de Specular level</i> | Defina quais unidades os valores F0. Entrada de specular level significa que será orientada por um mapa de entrada. |
| <b>Dielétrico F0</b> <i>0.0 - 0.08</i> | Se Valor constante for escolhido para Entrada dielétrica F0, este controle deslizante permite definir o valor global. |
| <b>Limpar revestimento</b> |  |
| <b>Habilitar Limpar Revestimento</b> <i>Falso/Verdadeiro</i> | Habilita uma camada de revestimento transparente adicional e simples na parte superior do material de entrada. |
| <b>Limpar Espessura Da Pelagem</b> <i>0.0 - 1.0</i> | Define a intensidade ou a intensidade da camada de revestimento transparente. |
| <b>Limpar Nível especular do revestimento</b> <i>0.0 - 1.0</i> | Define a aspereza da camada de revestimento transparente. |
| <b>Herdar normal da camada base</b> <i>Falso/Verdadeiro</i> | Defina se o clareamento ignora ou usa os normais do material de base. |
| <b>Emissivo</b> |  |
| <b>Habilitar Iluminação de Emissivo</b> <i>Verdadeiro/Falso</i> | Alterna a contribuição difusa da iluminação do emissivo. |
| <b>Intensidade de Emissivo</b> <i>0.0 - 10.0</i> | Define o multiplicador global para o mapa emissivo. |
| <b>Dispersão da Subsuperfície</b> |  |
| <b>Habilitar dispersão de subsuperfície</b> <i>Verdadeiro/Falso</i> | Alterna a dispersão da subsuperfície na renderização final.<br><br><i>Observação:</i> a dispersão da subsuperfície requer que o valor de entrada de <b>Translucidez</b> seja <i>maior que 0,0</i> |
| <b>Distância de dispersão</b> <i>0.0 - 1.0</i> | Ajusta a distância máxima do efeito de dispersão.<br><br><i>Observação:</i> este valor é multiplicado pelo valor de entrada <i>da Escala de distância de dispersão</b> <b>por canal de cor</i>. |
| <b>Turno Vermelho</b> <i>0.0 - 1.0</i> | Ajusta a intensidade do efeito Deslocamento de vermelho na dispersão. |
| <b>Rayleigh</b> <i>0.0 - 1.0</i> | Ajusta a intensidade do efeito Rayleigh na dispersão. |

## Exemplos

Todas as imagens foram geradas diretamente dentro do Designer, na viewport 2D, usando materiais da biblioteca [ativos do Substance 3D](https://substance3d.adobe.com/assets).

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/pbr-render-v2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-thermal-insulation-panel.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-ominous-obsidian.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-forest-gravel-1.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-chesterfield-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-carbon-fiber.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/plane-inclined-lumber-tiles.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/cylinder-medieval-leaded-glass-window.jpg" />
        </td>
    </tr>
</table>
