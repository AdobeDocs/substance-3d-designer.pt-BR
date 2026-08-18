---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/switching-your-shaders-to-opengl-core-profile.html"
breadcrumb-title: ''
description: Saiba como alternar sombreadores para o perfil OpenGL Core na exibição Substance 3D Designer 3D para obter compatibilidade e desempenho.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Switching your shaders to OpenGL Core Profile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alternando seus sombreadores para o perfil OpenGL Core
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# Alternando seus sombreadores para o perfil OpenGL Core

Desde a versão 2018.2.0, o visor 3D usa o perfil principal do OpenGL.\
Nesta ocasião, atualizamos alguns shaders que fornecemos com a aplicação da versão GLSL 120 para a versão GLSL 330.

Você pode querer atualizar seus próprios sombreadores para tirar vantagem das novas funções GLSL disponíveis, ou para tornar seu código GLSL mais moderno. Observe que no MacOS, os sombreadores antigos podem não funcionar mais.\
Para obter uma visão geral completa dos novos recursos, recomendamos que você analise a documentação oficial do OpenGL. Você pode, por exemplo, examinar a [Especificação de linguagem de Sombreamento OpenGL 3.30](https://www.khronos.org/registry/OpenGL/specs/gl/GLSLangSpec.3.30.pdf).\
Caso contrário, aqui está um guia rápido que irá ajudá-lo a converter seus shaders GLSL 1.20 em GLSL 3.30:

## Atualizar o número da versão

Primeiro, substitua (ou adicione-a na parte superior do arquivo, se ainda não tiver) sua diretiva `#version` anterior por `#version 330`.

### Substitua seu “atributo” e “variável” por “dentro” ou “fora”

Agora, as variáveis `attribute` e `varying` são declaradas explicitamente como `in` ou `out`, dependendo do estágio do sombreador:

No sombreador de vértices, `attribute`s dos vértices são declarados como `in`, enquanto `varying`s a serem passados para o sombreador de fragmentos são declarados como `out`.\
Por exemplo:

```
## version 120



attribute vec3 vertexPosition;

attribute vec3 vertexNormal;

attribute vec2 vertexUV;



varying vec3 fragmentNormal;

varying vec2 fragmentUV;
```


torna-se:

```
## version 330



in vec3 vertexPosition;

in vec3 vertexNormal;

in vec2 vertexUV;



out vec3 fragmentNormal;

out vec2 fragmentUV;
```


Da mesma forma no sombreador de fragmentos, a variação se torna dentro. Você também deve declarar uma variável out que substituirá gl\_FracColor (que não é mais embutida):

```
## version 120



varying vec3 fragmentNormal;

varying vec2 fragmentUV;



void main() {

...

gl_FragColor = vec4(myColor.rgb, 1.0);

}
```


torna-se:

```
## version 330



in vec3 fragmentNormal;

in vec2 fragmentUV;



out vec4 outColor; //you could choose any name you want here



void main() {

...

outColor = vec4(myColor.rgb, 1.0);

}
```


### Usar novas funções de pesquisa de textura

Com a nova versão da linguagem de sombreamento, a API de pesquisa de textura foi simplificada e aumentada.

As funções `texture1D()`, `texture2D()`, `texture3D()` e `textureCube()` se tornam sobrecargas de `texture()`.\
Da mesma forma, `texture2DLod()` torna-se `textureLod()`, `texture2DGrad()` torna-se `textureGrad()` e assim por diante.

Agora você também tem acesso a funções úteis, como `textureSize()` (para consultar o tamanho da amostra no texel), `textureOffset()` (para obter amostra dos vizinhos do local de destino), `textureFetch()` (para fornecer uma localização de amostra em pixels) e mais coisas.
