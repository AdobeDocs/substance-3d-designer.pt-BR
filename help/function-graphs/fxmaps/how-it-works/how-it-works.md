---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/how-it-works.html"
breadcrumb-title: ''
description: Saiba como o FXMaps funciona no Substance 3D Designer para aplicar gráficos de função ao textura para efeitos processuais.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > How it works
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Como funciona
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---


# Como funciona

Entender como um FX-Map funciona é a chave para dominar esse recurso poderoso.

Um gráfico FX-Map pode conter um ou mais dos três tipos de nó FX-Map: Quadrante, Iterar e Alternar. Desses nós, o que você provavelmente usará com mais frequência é o Quadrante, com o nó Iterado em um segundo próximo.

O nó Conjunto de parâmetros é o motor primário do FX-Maps. Cria o gráfico de árvore quádrupla da região principal em que os FX-Maps dependem, mas não é exibido como um. Visualmente, o gráfico de árvore quádrupla é mostrado na forma de uma Cadeia de Markov.

Ao renderizar o FX-Map, o gráfico FX-Map simplificado é “desempacotado” para se parecer com o gráfico grande, como uma árvore. O motor “anda” por toda a árvore quádrupla, trabalhando de cima para baixo, e depois da esquerda para a direita.

Os nós FX-Map não copiam e colam cegamente as imagens. Quando cada imagem é renderizada, todas as funções dinâmicas que ela tem são executadas. As funções afetam cada imagem renderizada pelo nó. Portanto, é possível dar a cada imagem individual uma rotação aleatória, um fator de escala ou vários outros ajustes.
