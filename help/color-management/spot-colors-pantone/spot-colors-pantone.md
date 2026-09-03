---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/color-management/spot-colors-pantone.html"
breadcrumb-title: ''
description: Saiba como usar as cores especiais do Pantone no Substance 3D Designer para uma correspondência precisa de cores em fluxos de trabalho de impressão e design.
helpx_creative_field: ""
helpx_description: Designer > Color Management > Spot Colors (Pantone)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cores especiais (Pantone)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---


# Cores especiais (Pantone)

As Cores especiais são um modo alternativo para a escolha de cores. Em vez do seletor de cores padrão RGB ou HSV, o Substance 3D Designer permite escolher cores dos Livros de Cores, combinando os sistemas existentes de gerenciamento e reprodução de cores. Isso permite garantir que as cores digitais usadas no Designer correspondam perfeitamente às dos produtos fabricados.

Atualmente, a Spot Colors oferece dezessete livros da Pantone.

## Gerenciamento de cores

Como as Cores Spot são feitas para reprodução e correspondência precisas de cores, é essencial que você configure o [Gerenciamento de Cores](../../color-management/color-management.md) para o Designer antes de começar a trabalhar. As cores especiais funcionam melhor com o gerenciamento de cores do <b>Adobe Color Engine (ACE)</b>, não com o OCIO. Eles funcionarão com o modo herdado, mas não é possível ter certeza de que serão exibidos corretamente se o monitor não estiver calibrado para sRGB.

Em resumo, a configuração do Gerenciamento de cores para cores especiais envolve o seguinte:

* Calibre seu monitor gerando ou obtendo o perfil ICC adequado.
* Ative o Gerenciamento de cores com Adobe Color Engine (ACE) nas Preferências do Designer.
* Defina as visualizações 2D e 3D para usar o perfil correto do monitor.
* Reinicie para que as alterações tenham efeito.
* Verifique a correspondência de cores entre o Designer e outro aplicativo Adobe, como o Adobe Illustrator ou o Photoshop. A cor “<b>Pantone Rhodamine Red C</b>” do primeiro livro da Pantone, Solid Coated, é um bom caso de teste, pois pode variar significativamente se o gerenciamento de cores não estiver correto.

>[!WARNING]
>
> **Cores de Miniatura**
> 
> As miniaturas de nós *não são gerenciadas por cor por padrão*, portanto, confie somente na exibição de cores 2D com o perfil correto. O gerenciamento de cores de miniatura pode ser ativado em Preferências, no Gerenciamento de cores do projeto, mas tem um pequeno custo de desempenho.

## Uso de cores especiais

### Alternar para cor especial do RGB

Mesmo que você configure o gerenciamento de cores, os seletores de cores ainda serão padronizados para os seletores de cores RGB ou HSV por padrão. Você precisa alterná-las manualmente para Cores especiais. Essa configuração é armazenada por parâmetro e até mesmo continua durante a exposição de um parâmetro.

1. Clique no botão ![](spot-colors-pantone.resources/spot-colors-pantone-01.png) <b>Tipo de seletor de cores</b> ao lado da amostra de cores do RGB.
1. Em vez de <b>cores RGB</b>, escolha qualquer <b>livro de cores</b> na lista suspensa.
1. O ícone do ![](spot-colors-pantone.resources/spot-colors-pantone-02.png) <b>Tipo de seletor de cores</b> é alterado, e sua interface é alterada para o modo de <b>Cores especiais</b>.

![Alternando para o modo de Cores especiais](spot-colors-pantone.resources/spot-colors-pantone-03.gif "Alternando para o modo de Cores especiais"){width="512px"}

### Escolher e encontrar cores especiais

Há algumas maneiras de localizar e escolher cores especiais em um livro de cores.

* Você pode usar as ![](spot-colors-pantone.resources/spot-colors-pantone-04.png) ![](spot-colors-pantone.resources/spot-colors-pantone-05.png) <b>setas para a esquerda e para a direita</b> em ambos os lados das páginas do livro para alternar entre as páginas. Você também pode clicar e arrastar na exibição da página para rolar entre as páginas.
* Você pode clicar em qualquer cor da página atual para selecioná-la. Muitas vezes, há mais cores disponíveis e é necessário rolá-las um pouco para baixo.
* Você pode usar a barra de pesquisa para pesquisar cores por nome ou número. Esta busca só combina com os nomes das cores no livro, não há lógica complexa acontecendo; pesquisando “cinza” só produzirá resultados com a palavra “cinza” em seu nome, você não verá nenhuma cor cinza que tenha apenas números em seu nome.
* Para obter uma interface maior e mais fácil de usar para o livro de cores, clique na caixa de visualização de cores entre o ícone do ![](spot-colors-pantone.resources/spot-colors-pantone-06.png) <b>Conta-gotas</b> e a ![](spot-colors-pantone.resources/spot-colors-pantone-04.png) <b>Seta para a esquerda</b>.

![Navegando cores especiais](spot-colors-pantone.resources/spot-colors-pantone-07.gif "Navegando cores especiais"){width="512px"}

### Seleção e conversão de cores especiais

As cores especiais podem ser escolhidas usando a ferramenta ![](spot-colors-pantone.resources/spot-colors-pantone-06.png) <b>Conta-gotas</b>. Quando estiver no modo de Cor Spot, isso significa que a cor do RGB de amostra será convertida para a Cor Spot correspondente mais próxima do livro atualmente selecionado.

A ferramenta <b>Conta-gotas</b> do Designer pode ser usada em qualquer lugar da tela, sem limitações. Portanto, isso significa que você pode usar o Designer como uma ferramenta de conversão de cores especiais,

Alternar Livros, ou até mesmo voltar para RGB de um livro de Cores Spot, converterá a cor atual para a correspondência mais próxima. Isso significa que é possível converter cores entre livros e vice-versa para RGB.

>[!WARNING]
>
> A conversão de cores especiais entre livros é uma operação com perdas. Fazer uma conversão de ida e volta muitas vezes não levará à mesma cor que você começou!

![Escolher e converter cores especiais](spot-colors-pantone.resources/spot-colors-pantone-08.gif "Escolher e converter cores especiais"){width="512px"}
