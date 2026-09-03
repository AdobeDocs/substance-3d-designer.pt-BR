---
title: Visualizador 3D
description: Designer > Gráficos de composição de Substance > Referência dos nós para gráficos de composição de Substance > Biblioteca de nós > Filtro > Efeito > Visualizador 3D
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1989'
ht-degree: 0%

---


# Visualizador 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de visualizador 3D](./3d-viewer.resources/3d-viewer-01.png "visualizador 3D")

<b>Entrada:</b> Filtro > Efeito

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Computa uma renderização 3D para um SDF especificado ou uma cena de interseção definida por um gráfico de função, com uma câmera personalizada e luz de ambiente.<br><br>Este nó é útil para criar e visualizar [Funções SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions) a serem usadas no nó [respingo de forma v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md).<br><br>Os auxiliares estão disponíveis para visualizar os principais atributos das formas no espaço.<br><br>Para usuários avançados, as funções personalizadas podem ser criadas para configurar a câmera e/ou a renderização 3D por pixel.

</td>
</tr>
</table>

>[!INFO]
> 
> Para saber mais sobre conceitos e fluxos de trabalho que envolvem Funções SDF, acesse a página dedicada: [Trabalhando com Funções SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Entradas

|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Ambiente</b> *Cor* | A imagem que deve ser projetada na esfera infinita usada como o ambiente da cena e usada para a iluminação do ambiente.<br><br>A projeção é <i>equiretangular</i>, a mesma usada pelos mapas de ambiente padrão do Designer disponíveis na categoria <b>Exibição 3D > ambientes HDRI</b> da Biblioteca.<br><br>Quando deixado desconectado, um ambiente padrão é usado.<br><br><i>Dica:</i> use uma imagem HDR (32 bits) para iluminação precisa. |
| <b>Entrada 1</b> *Cor* | Uma imagem que pode ser usada como amostra no gráfico de função <b>Saída personalizada</b> quando o parâmetro <b>Saída</b> estiver definido como &#39;Personalizado&#39;.<br><br>Use um nó [Cor de amostra](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) definido como &#39;Entrada de imagem 0&#39; para obter a amostra desta imagem. |
| <b>Entrada 2</b> *Cor* | Uma imagem que pode ser usada como amostra no gráfico de função <b>Saída personalizada</b> quando o parâmetro <b>Saída</b> estiver definido como &#39;Personalizado&#39;.<br><br>Use um nó [Cor de amostra](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) definido como &#39;Entrada de imagem 1&#39; para obter uma amostra desta imagem. |

<a name="outputs"></a>

## Saídas

|               |                                                                                                                                                                                                                                    |
|:--------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Saída</b> | A cena renderizada, usando a AOV selecionada no parâmetro <b>Saída</b>.<br><br><i>Observação:</i> para leituras precisas em algumas AOVs, verifique se a exibição 2D usa um espaço de cores linear e se o nó usa um formato de saída HDR de 32 bits. |

<a name="parameters"></a>

## Parâmetros

|                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:----------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Tipo de cena</b> *Inteiro* | O tipo de função usada para descrever as superfícies e as formas a serem renderizadas:<br>- <b>SDF:</b> Use uma função de campo de distância assinado (SDF), que pode descrever formas complexas.<br>- <b>Interseção:</b> Use funções de interseção, que são mais rápidas quando apenas formas primitivas simples são necessárias. |
| <b>Cena SDF</b> *Flutuante* | A função campo de distância assinado (SDF) que descreve as superfícies e formas na cena.<br><br>Use os nós na categoria [Funções SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions) da biblioteca para criar a função. |
| <b>Fazer interseção da cena</b> *Flutuante* | A função de interseção que descreve as superfícies e as formas da cena.<br><br>Funções de interseção para primitivos simples e operadores estão disponíveis nas pastas <b>3d_intersection</b> do pacote de biblioteca <b>3d_functions.sbs</b>.<br><br><i>Dica:</i> você pode acessar o pacote soltando qualquer nó SDF da biblioteca no Explorer. |
| <b>Saída</b> *Inteiro* | O tipo de renderização 3D que deve ser gerado pelo nó, comumente conhecido como AOVs (Variáveis de saída arbitrárias).<br><br>As AOVs disponíveis são:<br>- <b>Beleza:</b> O resultado final da renderização 3D, com cores e efeitos direcionados à arte.<br>- <b>WS normal:</b> Os normais de espaço do mundo das formas na cena.<br>- <b>TS normais:</b> Os normais de espaço tangente das formas na cena.<br>- <b>Posição:</b> A posição do espaço global das superfícies das formas na cena.<br>- <b>Distância:</b> a distância bruta entre a câmera e as formas na cena<br>- <b>Profundidade:</b> a distância assinada das formas do plano de destino da câmera, onde o plano sempre fica de frente para a câmera.<br>- <b>Cor:</b> a cor de base das formas (use o nó “Definir cor” para atribuir cores às formas na função da cena)<br>- <b>Material ID:</b> As IDs de material aplicadas às superfícies da forma (use o nó “Definir ID de material” para atribuir IDs de material a formas na função da cena)<br>- <b>Etapas de rastreamento de esfera:</b> Uma visualização da quantidade de etapas necessárias para definir a superfície de uma forma. Valores mais brilhantes significam que mais etapas foram necessárias.<br>- <b>Personalizado:</b> Crie uma função personalizada para calcular a cor da renderização por pixel.<br><br><i>Observação:</i> para obter leituras precisas em algumas AOVs, verifique se o Visualização 2D usa um espaço de cores linear e se o nó usa um formato de saída HDR de 32 bits. |
| <b>Saída personalizada</b> *Flutuante4* | O gráfico de função que define as cores RGBA por pixel da cena renderizada, como um valor de Precisão decimal 4.<br><br>Variáveis disponíveis:<br>- <code>scene.position</code> (Precisão decimal 3) A posição do espaço global das superfícies da cena.<br>- <code>cena.normal</code> (Precisão decimal 3) Os normais do espaço global das superfícies da cena.<br>- <code>scene.hit</code> (Booleano) Retorna &#39;True&#39; quando uma superfície é atingida por um raio de câmera.<br>- <code>view.origin</code> (Float3) A posição do espaço mundial por pixel da exibição da câmera.<br>- <code>view.direction</code> (Flutuante3) O vetor de avanço por pixel da visualização da câmera, de acordo com o modo de projeção. (E.g. Perspectiva ou ortográfica)<br>- <code>material.color</code> (Precisão decimal 3) A cor de base das superfícies da cena.<br>- <code>material.metalidade</code> (Precisão decimal) A metalidade das superfícies da cena.<br>- <code>material.rugosidade</code> (Precisão decimal) A aspereza das superfícies da cena.<br>- <code>material.id</code> (Inteiro) Os IDs de material das superfícies da cena.<br><br>As entradas de imagem do nó podem ser amostradas selecionando os seguintes slots de nó [Cor de amostra](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md):<br>- <b>Entrada de imagem 0</b> amostras Entrada 1.<br>- <b>Entrada de imagem 1</b> amostras Entrada 2. |
| <b>Rotação do ambiente</b> *Flutuante* | A rotação do <b>Ambiente</b>, em número de rotações. |
| <b>Modo de plano de fundo</b> *Inteiro* | Especifica a origem do plano de fundo da cena, desenhada onde nenhuma superfície de forma é visível.<br><br>- <b>Cor:</b> A &#39;Cor do plano de fundo&#39; plana.<br>- <b>Ambiente:</b> A imagem fornecida à entrada &#39;Ambiente&#39;, aplicada a uma esfera infinita usando a projeção equiretangular.  (Quando a entrada não está conectada, um ambiente padrão é usado.) |
| <b>Cor do plano de fundo</b> *Flutuante4* | A cor plana usada como plano de fundo da cena. |
| <b>Amostras IBL</b> *Inteiro* | A quantidade de amostras de luz executadas por amostra de câmera.<br><br>Um valor mais alto resulta em uma iluminação mais suave e precisa, o que prejudica o desempenho. |
| <b>Amostras de câmera</b> *Inteiro* | A quantidade de amostras de câmera executadas por pixel.<br><br>Este parâmetro afeta a qualidade da suavização de borda e a profundidade do efeito de campo.<br><br>Um valor mais alto resulta em uma imagem mais clara e menos barulhenta, em detrimento do desempenho. |
| <b>Etapas de raio marcial</b> *Inteiro* | A quantidade de etapas executadas no processo de traçado de esfera, a técnica de traçado de raio usada para detectar e desenhar as superfícies das formas.<br><br>Um valor mais alto resulta em superfícies precisas e consistentes (especialmente para formas complexas), em detrimento do desempenho.<br><br><i>Dica:</i> defina o parâmetro <b>Saída</b> para a AOV “Etapas de traçado de esfera” para visualizar as áreas das formas que exigem mais etapas. Essas áreas serão afetadas primeiro pela redução da quantidade de etapas. |
| <b>Etapas de marcação de raio secundário</b> *Inteiro* | A quantidade de etapas executadas no processo de traçado de esfera para calcular a difusão e a oclusão do specular a fim de desenhar sombras projetadas.<br><br>Um valor mais alto resulta em sombras mais precisas, o que prejudica o desempenho. |
| <b>Modo de câmera</b> *Inteiro* | O método de projetar a cena na imagem de renderização:<br><br>- <b>Perspectiva:</b> essa projeção transmite profundidade e permite efeitos de lente, como profundidade de campo.<br>- <b>Ortográfico:</b> essa projeção achata a cena, anulando a profundidade.<br>- <b>Função personalizada:</b> crie um gráfico de função para configurar uma câmera personalizada. |
| <b>Função de câmera</b> *Flutuante3* | O gráfico de função que define a transformação da câmera. Isso pode ser usado para configurar uma câmera personalizada.<br><br>A função deve <b>definir</b> estas variáveis:<br>- <code>exibir.origem</code> (Float3) A posição do espaço mundial por pixel da exibição da câmera.<br>- <code>view.direction</code> (Flutuante3) O vetor de avanço por pixel da visualização da câmera, de acordo com o modo de projeção. (E.g. perspectiva ou ortográfica)<br><br>As seguintes variáveis estão disponíveis para <b>get</b>:<br>- <code>camera.origin</code> (Float3) A posição do espaço global da câmera. (camera.direction * camera_distance + camera.target)<br>- <code>camera.direction</code> (Float3) A direção do espaço mundial da câmera, isto é, o vetor de avanço Y da câmera.<br>- <code>câmera.direita</code> (Float3) O vetor de direita X da câmera.<br>- <code>câmera.up</code> (Float3) O vetor Z-up da câmera.<br>- <code>camera.target</code> (Float3) A posição do espaço global do destino da câmera. |
| <b>Posição UV</b> *Flutuante2* | A posição no espaço de imagem 2D usada para inferir a posição e a direção da câmera que orbita a <b>Posição de destino</b>.<br><br><i>Dica:</i> esse parâmetro pode ser ajustado intuitivamente usando o <i>gizmo de posição</i> disponível na Exibição 2D quando o nó é selecionado. |
| <b>CDV</b> *Flutuante* | O campo de visão da câmera ortográfica (CDV), que afeta o fator de zoom. |
| <b>Distância focal</b> *Flutuante* | A distância focal da câmera, que afeta o fator de zoom e a profundidade do efeito de campo. |
| <b>Distância do destino</b> *Flutuante* | A distância em que a câmera deve descansar da <b>Posição de destino</b>.<br><br>Ajustar isso move a câmera na direção câmera para destino. |
| <b>Posição de destino</b> *Flutuante3* | A posição do alvo da câmera, para a qual a câmera está sempre orientada. |
| <b>Tonemapper</b> *Inteiro* | O algoritmo de mapeamento de tons que deve ser aplicado à renderização de cena.<br><br>- <b>Nenhum (Raw)<br>- <b>sRGB</b><br>- <b>AgX</b><br>- <b>ACES</b> |
| <b>Habilitar profundidade de campo</b> *Booleano* | Simula o efeito de lente da câmera “profundidade de campo” para a câmera de perspectiva.<br><br>Use os parâmetros <b>Número F</b> e <b>Distância de foco</b> para ajustar a abertura e o ponto focal do efeito, respectivamente.<br><br>O resultado também é afetado, mas a <b>Distância focal</b>. |
| <b>Número F</b> *Flutuante* | A <i>abertura</i> da câmera.<br><br>Um valor mais baixo resulta em uma <i>profundidade de campo</i> mais curta, ou seja, um intervalo de distância mais curto para objetos que são nítidos e um efeito de desfoque mais forte à medida que a distância desse intervalo aumenta. |
| <b>Distância de foco</b> *Flutuante* | Define a distância do ponto focal como uma distância da câmera ao longo de seu vetor à frente.<br><br>As superfícies dentro do intervalo dessa distância aparecerão nítidas, esse intervalo — a <i>profundidade de campo </i> — é definido pelo <b>número F</b>. |
| <b>Exposição (EV)</b> *Flutuante* | A quantidade de luz que chega ao sensor da câmera, isto é, a intensidade da iluminação na renderização.<br><br>Um valor mais baixo resulta em uma cena renderizada mais escura.<br><br>O &#39;Valor de Exposição&#39; (EV) se refere especificamente a quanta luz o sensor da câmera está <i>exposto</i>. |
| <b>Cor base</b> *Flutuante3* | A cor de base padrão para superfícies em que essa cor não é definida por seu SDF ou função de interseção. |
| <b>Aspereza</b> *Flutuante* | O valor padrão de aspereza para superfícies em que esse valor não é definido por seu SDF ou função de interseção. |
| <b>Metalidade</b> *Flutuante* | O valor padrão de metalidade para superfícies em que esse valor não é definido por seu SDF ou função de interseção. |
| <b>Opacidade dos auxiliares</b> *Flutuante* | A opacidade dos auxiliares 3D, onde um valor mais baixo resulta em auxiliares mais fracos. |
| <b>quadro delimitador</b> *Booleano* | Uma visualização de uma gaiola de seis lados que define os limites de toda a cena. O ideal é ter o menor tamanho possível, o que inclui completamente a cena.<br><br>Use o parâmetro <b>Tamanho do quadro delimitador</b> para ajustar o tamanho do compartimento.<br><br>O parâmetro <b>Colorir fora do quadro</b> permite visualizar facilmente as superfícies fora dessa gaiola, o que afeta o resultado do uso dessa cena no nó [respingo de forma v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md). (Consulte Dica de ferramenta “Tamanho do quadro delimitador”) |
| <b>Tamanho do quadro delimitador</b> *Flutuante3* | Define o tamanho XYZ do quadro delimitador.<br><br>Ajuste o quadro para a cena e, em seguida, aplique esses mesmos valores ao parâmetro <b>Tamanho do quadro associado ao SDF</b> do nó [respingo de forma v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) para garantir que todas as formas na cena sejam incluídas e desenhadas corretamente por esse nó. |
| <b>Colorir fora do quadro</b> *Booleano* | Aplica uma cor vermelha às superfícies fora do quadro delimitador.<br><br>Isso ajuda a verificar se a cena está totalmente incluída em seu quadro delimitador. |
| <b>Eixo</b> *Booleano* | Uma visualização dos eixos XYZ da cena como linhas coloridas começando na origem da cena. |
| <b>Grade</b> *Booleano* | Uma visualização de uma grade colocada nos eixos XY, onde o tamanho de uma célula em X e Y é uma unidade de cena. |
| <b>Transformar auxiliares</b> *Booleano* | Uma visualização da última rotação aplicada.<br><br>A visualização inclui<br>- <b>uma seta</b> que representa o vetor de direção do eixo de rotação e é colorida após as espessuras de cada eixo do espaço global.<br>- <b>Um arco</b> que representa o ângulo de rotação, ortogonal à seta que corresponde à sua cor. |
| <b>Isolamentos de SDF</b> *Booleano* | Uma visualização colorida das isolinhas de função do campo de distância assinado (SDF).<br><br>As isolinhas são linhas de repetição regular que representam o <i>campo de distância</i> da forma no plano XY em um determinado height.<br><br>Eles são úteis para verificar a <i>uniformidade do espaço</i> definido pela Função SDF.<br><br>Use os parâmetros <b>Frequência de isolamentos do SDF</b> e <b>Posição de isolamentos do SDF</b> para ajustar a densidade e o height das isolinhas. |
| <b>Frequência de isolamentos do SDF</b> *Precisão decimal* | A quantidade de repetições isoladas dentro de uma determinada distância.<br><br>Um valor mais alto resulta em linhas mais densas e mais finas. |
| <b>Posição de isolinhas do SDF</b> *Flutuante* | O height espacial mundial do plano XY usado para desenhar as isolinas.<br><br>Use esta opção para verificar o campo de distância da forma em várias elevações. |
| <b>Mín. distância da ocorrência</b> *Flutuante* | Define a distância mínima que se traduz em uma ocorrência para o processo de marcação de raio SDF.<br><br>Um valor baixo aumentará o número de etapas de marcação de raio. |

## Exemplos

<table style="border: none;">
    <tr style="width: 50%;">
        <td style="text-align: center">
            <img src="3d-viewer.resources/3d-viewer-02.jpg" alt="Exemplo 1" />
        </td>
        <td style="width: 50%;">
            <table style="border: none;">
                <tr style="vertical-align: top;">
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-03.jpg" alt="Exemplo 1" />
                    </td>
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-04.jpg" alt="Exemplo 2" />
                    </td>
                </tr>
                <tr style="vertical-align: top;">
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-05.jpg" alt="Exemplo 3" />
                    </td>
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-06.jpg" alt="Exemplo 4" />
                    </td>
                </tr>
            </table>
    </tr>
</table>
