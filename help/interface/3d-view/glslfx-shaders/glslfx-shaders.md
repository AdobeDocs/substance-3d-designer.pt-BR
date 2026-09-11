---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/glslfx-shaders.html"
breadcrumb-title: ''
description: Use sombreadores GLSLFX na exibição 3D do Substance 3D Designer para personalizar a renderização do material e os efeitos de visualização.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > GLSLFX Shaders
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sombreadores GLSLFX
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '3098'
ht-degree: 1%

---


# Sombreadores GLSLFX

Os arquivos GLSLFX fazem a ponte entre o aplicativo e os arquivos de sombreador glsl.\
Permite usar qualquer sombreador glsl sem ter que modificar o código.

## Formato de arquivo

O formato de arquivo GLSLFX é XML. Os comentários são aceitos.

### Nó de cabeçalho e raiz

O elemento de nó raiz XML é chamado <b>glslfx</b>.

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->

</glslfx>
```


### Corpo

#### Técnica

Elemento XML que descreve uma técnica. Uma técnica é uma variação do FX atual. Um GLSLFX pode conter várias técnicas, mas pelo menos uma técnica precisa ser definida.

A geometria será renderizada com uma das técnicas definidas pelo aplicativo.

+++Definição de elemento XML
Técnica <b>Nome:</b>

<b>Atributos:</b>

* nome: qualquer string usada para nomear a técnica

+++

O elemento XML pode ter vários filhos. Os elementos definidos em uma técnica substituem os elementos definidos globalmente.

Por exemplo, é usado para substituir alguns valores uniformes e obter variação de FX para essa técnica.

#### Passe de Renderização

Elemento XML que descreve uma passagem de renderização. Uma passagem de renderização descreve a renderização da geometria.

Uma técnica pode conter várias passagens de renderização que serão executadas sequencialmente. Uma técnica que não contém nenhuma passagem de renderização é equivalente a uma técnica que contém uma passagem de renderização “na tela”.

Os elementos definidos em uma passagem de renderização substituem os elementos definidos na técnica pai.

+++Definição de elemento XML
<b>Nome:</b> passagem

<b>Atributos:</b>

* saída

* fora da tela: a renderização será feita em destinos de renderização definidos pelo usuário

* Na tela: a renderização será feita no destino de renderização padrão

+++

#### Sombreamentos

Defina os arquivos de sombreador GLSL para cada tipo.

Definição do elemento XML:

+++Definição de elemento XML
<b>Nome:</b> sombreador

<b>Atributos:</b>

* tipo: o tipo de sombreador GLSL;

* nome do arquivo: o caminho do arquivo de sombreador glsl. Pode ser absoluto ou relativo ao arquivo GLSLFX;

* primitiveType: O método para renderizar a primitiva.


| Valor de &#39;type&#39; | Descrição |
| --- | --- |
| vértice | Sombreador de vértice |
| geometria | Sombreador de geometria |
| tess\_control | Sombreador de Controle de Mosaico |
| tess\_eval | Sombreador de Avaliação de Mosaico |
| fragmento | Sombreador de fragmento |



| Valor de &#39;primitiveType&#39; | Descrição |
| --- | --- |
| ponto | Renderizar como pontos |
| lineloop | Renderizar como loop de linha |
| patch[1..N] | Renderizar como correções com [1..N] vértices |


+++

#### Propriedades

Permite configurar parte do estado OpenGL.

+++Definição de elemento XML
Propriedade <b>Name:</b>

<b>Atributos:</b>

* nome: o nome da propriedade a ser definida. O nome é baseado na função OpenGL ou no nome glEnum:
  * Sintaxe Enums: sem o prefixo &#39;GL\_&#39;, em minúsculas. Exemplos: glEnable(GL\_BLEND\_ENABLE) => “”“, glDisable(GL\_CULL\_FACE) => “”&quot;
  * Sintaxe de funções: sem o prefixo &#39;gl&#39;, em minúsculas e com todas as palavras separadas com o caractere &#39;\_&#39;. Exemplo: glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => “”

* Sintaxe Enums: sem o prefixo &#39;GL\_&#39;, em minúsculas. Exemplos: glEnable(GL\_BLEND\_ENABLE) => “”“, glDisable(GL\_CULL\_FACE) => “”&quot;

* Sintaxe de funções: sem o prefixo &#39;gl&#39;, em minúsculas e com todas as palavras separadas com o caractere &#39;\_&#39;. Exemplo: glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => “”

* valor: o valor da propriedade.


| Valores de &#39;name&#39; | Valores de &#39;value&#39; | Descrição |
| --- | --- | --- |
| blend\_enabled | booleano | Ativar/desativar o modo de mesclagem |
|  | true |  |
|  | Falsa |  |
| blend\_func | string, string | Definir as funções de mesclagem de origem e destino |
|  | zero | para enumeração do OpenGL GL\_ZERO |
|  | um | para enumeração do OpenGL GL\_ONE |
|  | src\_color | para enumeração do OpenGL GL\_SRC\_COLOR |
|  | one\_minus\_src\_color | para enumeração do OpenGL GL\_ONE\_MINUS\_SRC\_COLOR |
|  | dst\_color | para enumeração do OpenGL GL\_DST\_COLOR |
|  | one\_minus\_dst\_color | para enumeração do OpenGL GL\_ONE\_MINUS\_DST\_COLOR |
|  | src\_alpha | para enumeração do OpenGL GL\_SRC\_ALPHA |
|  | one\_minus\_src\_alpha | para enumeração do OpenGL GL\_ONE\_MINUS\_SRC\_ALPHA |
|  | dst\_alpha | para enumeração do OpenGL GL\_DST\_ALPHA |
|  | one\_minus\_dst\_alpha | para enumeração do OpenGL GL\_ONE\_MINUS\_DST\_ALPHA |
|  | constante\_cor | para enumeração do OpenGL GL\_CONSTANT\_COLOR |
|  | one\_minus\_constant\_color | para enumeração do OpenGL GL\_ONE\_MINUS\_CONSTANT\_COLOR |
|  | constante\_alpha | para enumeração do OpenGL GL\_CONSTANT\_ALPHA |
|  | one\_minus\_constant\_alpha | para enumeração do OpenGL GL\_ONE\_MINUS\_CONSTANT\_ALPHA |
|  | src\_alpha\_saturate | para enumeração do OpenGL GL\_SRC\_ALPHA\_SATURATE |
|  | src1\_color | para enumeração do OpenGL GL\_SRC1\_COLOR |
|  | one\_minus\_src1\_color | para enumeração do OpenGL GL\_ONE\_MINUS\_SRC1\_COLOR |
|  | src1\_alpha | para enumeração do OpenGL GL\_SRC1\_ALPHA |
|  | one\_minus\_src1\_alpha | para enumeração do OpenGL GL\_ONE\_MINUS\_SRC1\_ALPHA |
| cull\_face\_enabled | booleano | Ativar/desativar a remoção de rosto |
|  | true |  |
|  | Falsa |  |
| selecionar\_rosto\_modo | string | Definir o modo de remoção de rosto |
|  | frente | para enumeração do OpenGL GL\_FRONT |
|  | trás | para enumeração do OpenGL GL\_BACK |
|  | frente\_e\_verso | para enumeração do OpenGL GL\_FRONT\_AND\_BACK |
| profundidade\_func | string | Definir a função de comparação de profundidade |
|  | nunca | para enumeração do OpenGL GL\_NEVER |
|  | menos | para enumeração do OpenGL GL\_LESS |
|  | desigual | para enumeração do OpenGL GL\_LEQUAL |
|  | igual | para enumeração do OpenGL GL\_EQUAL |
|  | diferente | para enumeração do OpenGL GL\_NOTEQUAL |
|  | gequal | para enumeração do OpenGL GL\_GEQUAL |
|  | maior | para enumeração do OpenGL GL\_GREATER |
|  | sempre | para enumeração do OpenGL GL\_ALWAYS |


+++

#### Uniformulários

Permite substituir alguns uniformes definidos globalmente ou na técnica pai. Isso permite alterar o comportamento do sombreador para essa técnica ou passagem de renderização.

Consulte a seção <b>Uniformes</b> abaixo para obter mais detalhes sobre a definição.

+++Exemplo


+++

## Destinos de renderização

Para passagens de renderização &#39;fora da tela&#39;, os destinos de renderização devem ser definidos na passagem de renderização.

+++Definição de elemento XML
Saída de <b>Nome:</b>

<b>Atributos:</b>

* anexo: O ponto de anexo do OpenGL, inspirado nos nomes do OpenGL:\
  GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
  GL\_PROFUNDIDADE\_ATTACHMENT => &#39;profundidade&#39;

anexo: O ponto de anexo do OpenGL, inspirado nos nomes do OpenGL:\
GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
GL\_PROFUNDIDADE\_ATTACHMENT => &#39;profundidade&#39;

* nome: o nome do destino de renderização.\
  Ele pode ser usado em um passo de renderização posterior para vincular esse destino de renderização como um sampler.

nome: o nome do destino de renderização.\
Ele pode ser usado em um passo de renderização posterior para vincular esse destino de renderização como um sampler.

* format: o formato interno do destino de renderização.

format: o formato interno do destino de renderização.

* clear: atributo opcional que define um valor clear.\
  Se presente, o destino de renderização será limpo para esse valor no início da passagem de renderização.\
  Se ausente, o destino de renderização manterá seu conteúdo anterior.

+++

>[!NOTE]
>
> Os destinos de renderização de cores são proibidos em um passo de renderização “na tela”, mas um destino de renderização de profundidade pode ser compartilhado com qualquer passo de renderização (mas é provável que ele interrompa a renderização ao misturar vários materiais na cena).

<b>Sobre formatos</b>

Para formatos de profundidade, todos os formatos OpenGL somente de profundidade (sem estêncil) são compatíveis:

* GL\_PROFUNDIDADE\_COMPONENT16 => &#39;profundidade26&#39;
* GL\_PROFUNDIDADE\_COMPONENT24 => &#39;profundidade34&#39;
* GL\_PROFUNDIDADE\_COMPONENT32 => &#39;profundidade42&#39;
* GL\_PROFUNDIDADE\_COMPONENT32F => &#39;profundidade42f&#39;

Para os formatos de cores, o nome é baseado nos nomes enum do OpenGL, sem o prefixo &#39;GL\_&#39;, em minúsculas.\
Não há suporte para três formatos de canal (RGB); em vez disso, use um formato RGBA.\
Profundidade de bits por canal compatível:

* Inteiro sem sinal normalizado: 8, 16
* Ponto flutuante: 16, 32

Uma exceção a essas regras é o formato GL\_R11F\_G11F\_B10F, que é compatível.:

* GL\_RGBA8 => &#39;rgba8&#39;
* GL\_RGBA16F => &#39;rgba16f&#39;
* GL\_SRGB8\_ALPHA8 => &#39;srgb8\_alpha8&#39;
* GL\_R11F\_G11F\_B10F => &#39;r11f\_g11f\_b10f&#39;
* GL\_RG16 => “rg16”

### Amostragem

Permitir que o substitua alguns amostradores definidos globalmente, eles não podem ser definidos em uma técnica. Isso permite definir um uso do sampler para essa passagem de renderização ou para ler de um destino de renderização de uma passagem de renderização anterior.

Consulte a seção <b>Samplers</b> para obter mais detalhes sobre suas definições.

+++Exemplo


+++

## Formato de vértice de entrada

Isso permite definir a semântica de cada atributo definido no sombreador de vértice.

<b>Definição de Elemento XML:</b>

Nome: &#39;vertexformat&#39;

Atributos:

* &#39;name&#39;: O nome do atributo conforme definido no sombreador de vértice.
* &#39;semantic&#39;: A semântica do atributo.

| Valor &#39;semântico&#39; | Descrição |
| --- | --- |
| posição | Posição do vértice (float3) |
| normal | Vértice normal (float3) |
| texcoord[0..N] | Buffer de coordenadas de textura de vértice N (float2) |
| tangente[0..N] | Buffer tangente de vértice N (float4) |
| binormal[0..N] | Buffer binormal de vértice N (float4) |

Exemplo:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- INPUT VERTEX FORMAT -->

     <vertexformat name="iVS_Position" semantic="position"/>

     <vertexformat name="iVS_Normal" semantic="normal"/>

     <vertexformat name="iVS_UV" semantic="texcoord0"/>

     <vertexformat name="iVS_Tangent" semantic="tangent0"/>

     <vertexformat name="iVS_Binormal" semantic="binormal0"/>

</glslfx>
```


## Amostragem

Isso permite definir o uso de cada amostrador.\
É usado pelo aplicativo para saber qual textura definir nos classificadores especificados.

<b>Definição de Elemento XML:</b>

Nome: &#39;sampler&#39;

Atributos:

* &#39;name&#39;: O nome da variável do sampler no arquivo shader.
* &#39;uso&#39;: O uso do sampler. Corresponde ao uso especificado no nó Saída do gráfico.

| Valor de &#39;uso&#39; | Descrição |
| --- | --- |
| difusa | Mapa difuso |
| opacidade | Mapa de opacidade |
| emissivo | Mapa emissivo |
| ambientoclusão | Mapa de oclusão do ambiente |
| ambiente | Mapa do ambiente |
| máscara | Mapa de máscara |
| detalhadonormal | Detalhar mapa normal |
| normal | Mapas normais |
| mapeamento | Mapa de relevo |
| height | mapa de heights |
| deslocamento | mapa de deslocamentos |
| specularlevel | mapa de speculares leveis |
| specularcolor | mapa de cores do specular |
| specular | mapa de specular |
| glossiness | Mapa de textura reluzente |
| de aspereza | Mapa de aspereza |
| anisotropylevel | Mapa do nível de anisotropia |
| anisotropiângulo | Mapa do ângulo de anisotropia |
| transmissivo | Mapa transmissivo |
| reflexo | Mapa de reflexão |
| refração | Mapa de refração |
| ambiente | Mapa do ambiente (mapa do cubo) |
| panorama | O Mapa Panorâmico (Mapa Da Latitude/Longitude) |
| bluenoisemask | Uma textura de pontilhamento de 256x256 |

* Há suporte para vários usos.
  * Exemplo:

```
   <!-- SAMPLERS -->

    <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <!-- ... -->
```


&#39;isHidden&#39;: Booleano que indica se o sampler deve aparecer na GUI

* Exemplo:

```
     <!-- SAMPLERS -->

    <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <!-- ... -->
```


Modo de quebra automática:

<table data-preserve-html="true"><tbody><tr><th>Nome</th><th>Valor</th></tr><tr><td rowspan="4">textura_wrap_s, textura_wrap_t, textura_wrap_r<br/><br/><br/></td><td>clamp_to_edge</td></tr><tr><td>clamp_to_border</td></tr><tr><td colspan="1">mirrored_repeat</td></tr><tr><td colspan="1">repetir<br/><br/></td></tr></tbody></table>

Filtro de Textura

<table data-preserve-html="true"><tbody><tr><th>Nome</th><th>Valor</th></tr><tr><td rowspan="6">textura_min_filter, textura_mag_filter<br/><br/><br/></td><td>mais próximo</td></tr><tr><td>linear</td></tr><tr><td colspan="1">nearest_mipmap_nearest</td></tr><tr><td colspan="1">linear_mipmap_nearest</td></tr><tr><td colspan="1">nearest_mipmap_linear</td></tr><tr><td colspan="1">linear_mipmap_linear</td></tr></tbody></table>

Exemplo:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- SAMPLERS -->

     <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <sampler name="heightMap" usage="height"/>

     <sampler name="normalMap" usage="normal"/>

     <sampler name="detailNormalMap" usage="detailNormal"/>

     <sampler name="environmentMap" usage="environment"/>

     <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <sampler name="sssDiffuseMap" usage="sssDiffuse"/>

</glslfx>
```


## Uniformulários

Isso permite que você adicione informações adicionais em cada uniforme de sombreador.

<b>Definição de Elemento XML:</b>

Nome: &#39;uniforme&#39;

Atributos:

&#39;nome&#39;: o nome do uniforme no arquivo de sombreador.

| Valor &#39;semântico&#39; | Descrição |
| --- | --- |
| mundo | Matriz Mundial (float16) |
| worldinversetranspose | Matriz mundial de transposição inversa (float16) |
| worldviewprojection | Matriz de projeção do World View (float16) |
| viewinverse | Matriz Inversa Mundial (float16) |
| worldview | Matriz do World View (float16) |
| modelview | Matriz de visualização de modelo (float16) |
| projeção | Matriz de Projeção (float16) |
| ambiente | Cor do ambiente da cena (float3) |
| posição da luz[0..N] | Posição da luz nº da cena (float3) |
| lightcolor[0..N] | Cor da luz n da cena (float3) |
| lightintensity[0..N] | Intensidade da luz n da cena (flutuante) |
| globaltime | Tempo atual em segundos (float) |
| resolução | Resolução do visor (int2) |
| rato | Posição do mouse (int2) |
| samplespostablesize | Número de amostras a serem usadas para calcular a iluminação ambiente (int) |
| irradianceshcoefs | A matriz de vetores harmônicos esféricos (float3[10]) |
| panoramamipmapheight | Número de níveis do mipmap no mapa panorâmico (flutuante) |
| panoramarotation | Ângulo Ângulo de rotação do mapa de panorama (flutuante) |
| intensidade de panorama | Intensidade do mapa de panorama (flutuante) |
| computebinormalinfragmentshader | O binormal é calculado por fragmento? (se não for então por vértice) (bool) |
| isdirectxnormal | O formato de mapa normal é DirectX? (bool) |
| uvwscale | Valores de escala de u, v, w (float3) |
| renderuvtile | Renderizar apenas 1 bloco UV? (bool) |
| uvtilecoords | Coordenada do ladrilho UV a ser renderizado (int2) |

&#39;semântica&#39;: A semântica do uniforme. (Todas as matrizes são float16).

Exemplo:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- MATRICES -->

     <uniform name="worldMatrix" semantic="world"/>

     <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

     <uniform name="worldViewMatrix" semantic="worldview"/>

     <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

     <uniform name="viewInverseMatrix" semantic="viewinverse"/>

     <uniform name="modelViewMatrix" semantic="modelview"/>

     <uniform name="projectionMatrix" semantic="projection"/>

</glslfx>
```


Exemplo:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>

</glslfx>
```


### Outros parâmetros

Outras informações adicionais podem ser adicionadas a cada uniforme para:

* definir o valor padrão
* valores do grampo
* controlar a forma como o uniforme será apresentado no pedido:
* definir o rótulo
* defina as informações do widget usadas para editar o valor no aplicativo:
* nome do widget, mínimo, máximo, etapa de incremento/decremento
* uniformes de grupo nos widgets de grupo

Como os Uniformes podem ser substituídos por cada técnica, permite exibir uma configuração de interface gráfica específica para cada técnica.

<b>Definição de Elemento XML:</b>

Nome: &#39;uniforme&#39;

Atributos:

* &#39;nome&#39;: o nome do uniforme no arquivo de sombreador.
* &#39;default&#39;: O valor padrão uniforme
* &#39;min&#39;: o valor mínimo do intervalo de validade
* &#39;max&#39;: O valor máximo do intervalo de validade
* &#39;guiName&#39;: O nome do uniforme na interface gráfica do aplicativo
* &#39;guiGroup&#39;: O nome do grupo para colocar o uniforme na interface gráfica do aplicativo
* &#39;guiWidget&#39;: o nome do widget usado para editar o valor uniforme na interface gráfica do aplicativo

| Valor de &#39;guiWidget&#39; | Descrição |
| --- | --- |
| corredor | Widget de controle deslizante para floatN |
| ângulo | Widget de ângulo para flutuar |
| cores | Widget de cor para cor float3, float4 |
| caixa de seleção | Widget CheckBox para bool |

* &#39;guiMin&#39;: O valor mínimo do widget
* &#39;guiMax&#39;: O valor máximo do widget

## Exemplo: mosaico/paralaxe

### Arquivo de sombreador de vértices da paralaxe

Localizado em .\tessellation\_parallax\parallax\vs.glsl

Conteúdo:

> #version 120

atributo vec4 iVS\_Position;\
atributo vec4 iVS\_Normal;\
atributo vec2 iVS\_UV;\
atributo vec4 iVS\_Tangent;\
atributo vec4 iVS\_Binormal;

variando vec3 iFS\_Normal;\
variando vec2 iFS\_UV;\
variando vec3 iFS\_Tangent;\
variando vec3 iFS\_Binormal;\
variando vec3 iFS\_PointWS;

uniforme mat4 worldMatrix;\
uniforme mat4 worldViewProjMatrix;

void main()\
{\
gl\_Position = worldViewProjMatrix \&#42; iVS\_Position;\
iFS\_Normal = iVS\_Normal.xyz;\
iFS\_UV = iVS\_UV;\
iFS\_Tangent = iVS\_Tangent.xyz;\
iFS\_Binormal = iVS\_Binormal.xyz;\
iFS\_PointWS = (worldMatrix \&#42; iVS\_Position).xyz;\
}

### Arquivo de Sombreador de Vértice de Mosaico

Localizado em .\tessellation\_parallax\tessellation\vs.glsl

Conteúdo:

>> 

#version 120

atributo vec4 iVS\_Position;\
atributo vec4 iVS\_Normal;\
atributo vec2 iVS\_UV;\
atributo vec4 iVS\_Tangent;\
atributo vec4 iVS\_Binormal;

variando vec4 oVS\_Normal;\
variando vec2 oVS\_UV;\
variando vec4 oVS\_Tangent;\
variando vec4 oVS\_Binormal;

void main()\
{\
gl\_Position = iVS\_Position\
oVS\_Normal = iVS\_Normal;\
oVS\_UV = iVS\_UV;\
oVS\_Tangent = iVS\_Tangent;\
oVS\_Binormal = iVS\_Binormal;\
}

### Arquivo de Sombreador de Controle de Mosaico

Localizado em .\tessellation\_parallax\tessellation\tcs.glsl

Conteúdo:

>> 

#version núcleo 400\
#extension GL\_ARB\_tessellation\_shader : habilitar

layout(vértices = 3) out;

em vec4 oVS\_Normal[];\
em vec2 oVS\_UV[];\
em vec4 oVS\_Tangent[];\
em vec4 oVS\_Binormal[];

out vec4 oTCS\_Normal[];\
out vec2 oTCS\_UV[];\
out vec4 oTCS\_Tangent[];\
out vec4 oTCS\_Binormal[];

fator de mosaico de flutuador uniforme;

void main()\
{\
gl\_TessLevelOuter[0] = tessellationFactor;\
gl\_TessLevelOuter[1] = tessellationFactor;\
gl\_TessLevelOuter[2] = tessellationFactor;\
gl\_TessLevelInner[0] = tessellationFactor;\
gl\_out[gl\_InvocationID].gl\_Position = gl\_in[gl\_InvocationID].gl\_Position;

oTCS\_Normal[gl\_InvocationID] = oVS\_Normal[gl\_InvocationID];\
oTCS\_UV[gl\_InvocationID] = oVS\_UV[gl\_InvocationID];\
oTCS\_Tangent[gl\_InvocationID] = oVS\_Tangent[gl\_InvocationID];\
oTCS\_Binormal[gl\_InvocationID] = oVS\_Binormal[gl\_InvocationID];\
}

### Arquivo de Sombreador de Avaliação do Mosaico

Localizado em .\tessellation\_parallax\tessellation\tcs.glsl

Conteúdo:

>> 

#version núcleo 400

layout(triângulos, igual\_espaçamento, ccw) em;

em vec4 oTCS\_Normal[];\
em vec2 oTCS\_UV[];\
em vec4 oTCS\_Tangent[];\
em vec4 oTCS\_Binormal[];

uniforme mat4 worldMatrix;\
uniforme mat4 worldViewProjMatrix;

sampler2D heightMap uniforme;

revestimento de flutuador uniforme = 1.0f;\
heightMapScale de flutuação uniforme = 1.0f;

out vec3 iFS\_Normal;\
out vec2 iFS\_UV;\
out vec3 iFS\_Tangent;\
out vec3 iFS\_Binormal;\
out vec3 iFS\_PointWS;

vec3 interpolate3D(vec3 v0, vec3 v1, vec3 v2, vec3 uvw)\
{\
return uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2;\
}

vec2 interpolate2D(vec2 v0, vec2 v1, vec2 v2, vec3 uvw)\
{\
return uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2;\
}

void main()\
{\
vec3 uvw = gl\_TessCoord.xyz;

vec3 newPos = interpolate3D(gl\_in[0].gl\_Position.xyz, gl\_in[1].gl\_Position.xyz, gl\_in[2].gl\_Position.xyz, uvw);\
vec3 newNormal = normalize(interpolate3D(oTCS\_Normal[0].xyz, oTCS\_Normal[1].xyz, oTCS\_Normal[2].xyz, uvw));\
vec3 newTangent = normalize(interpolate3D(oTCS\_Tangent[0].xyz, oTCS\_Tangent[1].xyz, oTCS\_Tangent[2].xyz, uvw));\
vec3 newBinormal = normalize(interpolate3D(oTCS\_Binormal[0].xyz, oTCS\_Binormal[1].xyz, oTCS\_Binormal[2].xyz, uvw));\
vec2 newUV = interpolate2D(oTCS\_UV[0], oTCS\_UV[1], oTCS\_UV[2], uvw);

float heightTexSample = texture(heightMap, newUV \&#42; tiling).x \&#42; 2.0 - 1.0;\
newPos += newNormal \&#42; heightTextSample \&#42; heightMapScale;

vec4 obj\_pos = vec4(newPos, 1);\
gl\_Position = worldViewProjMatrix \&#42; obj\_pos;

iFS\_UV = newUV \&#42; tiling;\
iFS\_Tangent = newTangent;\
iFS\_Binormal = newBinormal;\
iFS\_Normal = newNormal;\
iFS\_PointWS = (worldMatrix \&#42; obj\_pos).xyz;\
}

### Arquivo sombreador de fragmentos

Localizado em .\tessellation\_parallax\fs.glsl

Conteúdo:

>> 

#version 120

// #define ALG\_NORMAL\_DIRECTX\
#define ALG\_NORMAL\_OPENGL

#ifdef ALG\_NORMAL\_DIRECTX\
// #define FLIP\_NORMAL\_X\
#define FLIP\_NORMAL\_Y\
// #define FLIP\_NORMAL\_Z\
#endif //#ifdef ALG\_NORMAL\_DIRECTX

#ifdef ALG\_NORMAL\_OPENGL\
// #define FLIP\_NORMAL\_X\
#define FLIP\_NORMAL\_Y\
// #define FLIP\_NORMAL\_Z\
#endif //#ifdef ALG\_NORMAL\_OPENGL

variando vec3 iFS\_Normal;\
variando vec2 iFS\_UV;\
variando vec3 iFS\_Tangent;\
variando vec3 iFS\_Binormal;\
variando vec3 iFS\_PointWS;

Lâmpada vec3 uniforme0Pos = vec3(0.0f,0.0f,70.0f);\
Lâmpada vec30Color uniforme = vec3(1.0f,1.0f,1.0f);\
Lâmpada vec3 uniforme1Pos = vec3(70.0f,0.0f,0.0f);\
Lâmpada vec3 uniforme1Color = vec3(0.198f,0.198f,0.198f);\
flipNormal bool uniforme = true;\
uniformemente float TilingDetail = 3.0f;\
SpecExpon de flutuação uniforme = 50,0;\
flutuador uniforme Ks = 1,0;\
uniforme int parallax\_mode = 0;\
tessellationFactor de flutuador uniforme = 4,0;\
heightMapScale de flutuação uniforme = 1.0f;\
uniformemente float Profundidade\_detail = 0.5f;\
flutuador uniforme Kr = 0,5f;\
uniforme int KF\_on = 1;\
flutuador uniforme KFs = 1.0f;\
vec3 AmbiColor uniforme = vec3(0.07f,0.07f,0.07f);\
revestimento de flutuador uniforme = 1.0f;\
uniforme int enableTilingInFS = 0;

sampler2D heightMap uniforme;\
sampler2D normalMap uniforme;\
sampler2D uniforme detailNormalMap;\
sampler2D emissiveMap uniforme;\
sampler2D diffuseMap uniforme;\
sampler2D specularMap uniforme;\
sampler2D opacityMap uniforme;\
samplerCube environmentMap uniforme;

uniforme mat4 worldMatrix;\
uniforme mat4 worldInverseTransposeMatrix;\
MatrizInversauniforme de visualização mat4;

vec4 litFct(float NdotL, float NdotH, float specExp)\
{\
ambiente flutuante = 1,0;\
float diffuse = max(NdotL, 0.0);\
specular flutuante = step(0.0, NdotL) \&#42; pow(max(0.0, NdotH), specExp);\
return vec4(ambiente, difuso, specular, 1.0);\
}

vec3 lerpFct(vec3 v0, vec3 v1, porcentagem de flutuação)\
{\
retornar v0 + (v1-v0) \&#42; por cento;\
}

// Phong Sombreamento\
void phong\_sombreamento(\
em vec3 LightColor,\
em vec3 normalWS,\
em vec3 pointToLightDirWS,\
em vec3 pointToCameraDirWS,\
inout vec3 DiffuseContrib,\
inout vec3 SpecularContrib)\
{\
vec3 Hn = normalize(pointToCameraDirWS + pointToLightDirWS);\
vec4 litV = litFct(dot(normalWS, pointToLightDirWS), dot(normalWS, Hn), SpecExpon);\
DiffuseContrib = litV.y \&#42; LightColor;\
SpecularContrib = litV.y \&#42; litV.z \&#42; Ks \&#42; LightColor;\
}

vec3 fixNormalSample(vec3 v)\
{\
resultado de vec3 = v - vec3(0,5,0,5,0,5);

#ifdef FLIP\_NORMAL\_X\
result.x = -result.x;\
#endif // ifdef FLIP\_NORMAL\_X\
#ifdef FLIP\_NORMAL\_Y\
result.y = -result.y;\
#endif // ifdef FLIP\_NORMAL\_Y\
#ifdef FLIP\_NORMAL\_Z\
result.z = -result.z;\
#endif // ifdef FLIP\_NORMAL\_Z

resultado de retorno;\
}

vec3 normalVecOSToWS(vec3 normal)\
{\
retorno normal;\
}

void main()\
{\
vec3 cameraPosWS = viewInverseMatrix[3].xyz;\
vec3 pointToLight0DirWS = normalize(Lamp0Pos - iFS\_PointWS);\
vec3 pointToLight1DirWS = normalize(Lamp1Pos - iFS\_PointWS);\
vec3 pointToCameraDirWS = normalize(cameraPosWS);\
vec3 normalOS = normalize(iFS\_Normal);\
vec3 tangentOS = normalize(iFS\_Tangent);\
vec3 binormalOS = normalize(iFS\_Binormal);

// ------------------------------------------\
// Verifique se o TBN está Orthonormalizado\
binormalOS = normalize(cross(normalOS, tangentOS));\
tangentOS = normalize(cross(binormalOS, normalOS));

vec3 cumulatedNormalOS = normalOS;

// ------------------------------------------\
// Atualizar UV\
float a = dot(normalOS,-pointToCameraDirWS);\
vec3 s = vec3(dot(pointToCameraDirWS,tangentOS), dot(pointToCameraDirWS,binormalOS), a);\
vec2 uv = enableTilingInFS == 0 ? iFS\_UV : (iFS\_UV \&#42; lado a lado);\
float height = textura2D(heightMap,uv).x \&#42; 2.0 - 1.0 ;\
float parallax = parallax\_mode == 0 ? (tessellationFactor / 100000.f + heightMapScale / 500.f) : (heightMapScale / 50.f);\
uv += (height \&#42; s.xy \&#42; paralaxe) ;

// ------------------------------------------\
// Adicionar Normal a partir de normalMap\
vec3 normalTS = textura2D(normalMap,uv).xyz;\
normalTS = fixNormalSample(normalTS);\
vec3 normalMapOS = normalTS.x\&#42;tangentOS + normalTS.y\&#42;binormalOS;\
cumulatedNormalOS = cumulatedNormalOS + normalMapOS;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

// ------------------------------------------\
// Adicionar o mapa normal detalhado\
vec3 normalDetailTS = textura2D(detailNormalMap,uv\&#42;TilingDetail).xyz;\
normalDetailTS = fixNormalSample(normalDetailTS);\
variável vec3NormalDetailTS = lerpFct(vec3(0.0,0.0,0.5),normalDetailTS,Profundidade\_detail);\
vec3 normalDetailOS = variableNormalDetailTS.x\&#42;tangentOS + variableNormalDetailTS.y\&#42;binormalOS;\
cumulatedNormalOS = cumulatedNormalOS + normalDetailOS;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

if (length(normalTS)&lt;0,0001)\
cumulatedNormalOS = normalOS;

vec3 cumulatedNormalWS = normalVecOSToWS(cumulatedNormalOS);

// ------------------------------------------\
// Calcular Difusão e Specular

// Contribuição clara 0\
vec3 diffContrib = vec3(0, 0, 0);\
vec3 specContrib = vec3(0, 0, 0);\
phong\_sombreamento(Lamp0Color, cumulatedNormalWS, pointToLight0DirWS, pointToCameraDirWS, diffContrib, specContrib);

// Contribuição Light 1\
vec3 diffContrib2 = vec3(0, 0, 0);\
vec3 specContrib2 = vec3(0, 0, 0);\
phong\_sombreamento(Lamp1Color, cumulatedNormalWS, pointToLight1DirWS, pointToCameraDirWS, diffContrib2, specContrib2);

diffContrib += diffContrib2;\
specContrib += specContrib2;

vec4 diffuseColor = texture2D(diffuseMap,uv);

vec3 specularColor = textura2D(specularMap,uv).rgb;\
vec3 R = reflect(pointToCameraDirWS,cumulatedNormalWS);\
vec3 reflColor = Kr \&#42; textureCube(environmentMap,R.xyz).bgr;

float FallofRefl

if (KFs >= 0,0)\
FallofRefl = max((1-dot(pointToCameraDirWS/(KFs),cumulatedNormalWS)),0)\&#42;KF\_on;\
senão\
FallofRefl = (1-max(((1-dot(pointToCameraDirWS/(-KFs),cumulatedNormalWS))),0))\&#42;KF\_on;

if (KF\_on == 0)\
FallofRefl=1.0;

vec3 Ambiant\_final = diffuseColor.rgb\&#42;AmbiColor;

// ------------------------------------------\
emissivo vec3 = textura2D(emissiveMap,uv).xyz;

vec3 finalcolor = Ambiant\_final\
+ specularColor\&#42;specContrib\
+ diffuseColor.rgb\&#42;diffContrib\
+ (reflColor\&#42;specularColor\&#42;FallofRefl)\
+ emissivo;

// Cor final\
vec4 finalColor4 = vec4(finalcolor, textura 2D(opacityMap,uv));

gl\_FragColor = finalColor4;\
}

### Arquivo GLSLFX

O arquivo glslfx define duas técnicas para renderizar a geometria:

* Utiliza-se a técnica de mosaico de hardware
* O outro, baseado em um efeito de paralaxe que será usado como substituto se o hardware do usuário não for compatível com o mosaico.

Localizado em .\tessellation\_parallax\fs.glsl

Conteúdo:

```
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE sbsbatchnode SYSTEM "glslfx.dtd">

<glslfx version="1.0.0" author="allegorithmic.com">



    <!-- TECHNIQUES -->

    <technique name="Tesselation">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/tessellation/vs.glsl" primitiveType="patch4"/>

        <shader type="tess_control" filename="tessellation_parallax/tessellation/tcs.glsl"/>

        <shader type="tess_eval" filename="tessellation_parallax/tessellation/tes.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="0" max="0" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="0" max="0" />

        <uniform name="tessellationFactor" guiName="Tessellation Factor" default="4" min="1" max="64" guiStep="1" guiWidget="slider"/>

    </technique>



    <technique name="Parallax">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/parallax/vs.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="1" max="1" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="1" max="1" />



    </technique>



    <!-- INPUT VERTEX FORMAT -->

    <vertexformat name="iVS_Position" semantic="position"/>

    <vertexformat name="iVS_Normal" semantic="normal"/>

    <vertexformat name="iVS_UV" semantic="texcoord0"/>

    <vertexformat name="iVS_Tangent" semantic="tangent0"/>

    <vertexformat name="iVS_Binormal" semantic="binormal0"/>



    <!-- SAMPLERS -->

    <sampler name="diffuseMap" usage="diffuse"/>

    <sampler name="heightMap" usage="height"/>

    <sampler name="normalMap" usage="normal"/>

    <sampler name="detailNormalMap" usage="detailNormal"/>

    <sampler name="emissiveMap" usage="emissive"/>

    <sampler name="specularMap" usage="specular"/>

    <sampler name="opacityMap" usage="opacity"/>

    <sampler name="environmentMap" usage="environment"/>



    <!-- MATRICES -->

    <uniform name="worldMatrix" semantic="world"/>

    <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

    <uniform name="worldViewMatrix" semantic="worldview"/>

    <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

    <uniform name="viewInverseMatrix" semantic="viewinverse"/>

    <uniform name="modelViewMatrix" semantic="modelview"/>

    <uniform name="projectionMatrix" semantic="projection"/>



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>



    <!-- UNIFORMS -->

    <uniform name="tiling" guiName="Tiling" default="1" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="heightMapScale" guiGroup="Height" guiName="Scale" default="1" min="0" guiWidget="slider" guiMin="-50" guiMax="50" />

    <uniform name="TilingDetail" guiGroup="Detail Normal" guiName="Tiling" default="3" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="Depth_detail" guiGroup="Detail Normal" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.05" guiWidget="slider"/>

    <uniform name="SpecExpon" guiGroup="Specular" guiName="Power" default="50" min="1" guiWidget="slider" guiMax="128"/>

    <uniform name="Ks" guiGroup="Specular" guiName="Intensity" default="1" min="0" guiWidget="slider" guiMax="3"/>

    <uniform name="Kr" guiGroup="Reflection" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.01" guiWidget="slider"/>

    <uniform name="KF_on" guiGroup="Reflection" guiName="Falloff" default="1" min="0" max="1" guiStep="1" guiWidget="slider"/>

    <uniform name="KFs" guiGroup="Reflection" guiName="Falloff Size" default="1" min="-1" max="1" guiStep="0.05" guiWidget="slider"/>



</glslfx>
```
