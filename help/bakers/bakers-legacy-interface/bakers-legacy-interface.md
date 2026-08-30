---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: Conheça a interface herdada do Substance 3D Designer baker para usuários familiarizados com versões mais antigas.
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Interface herdada de baker
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 4%

---


# Interface herdada de baker

Esta é a descrição da interface do baker disponível nas versões do [Adobe Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html) anteriores à 6.0.4.

## Visão geral

![](bakers-legacy-interface.resources/image2017-3-13-9-33-40.png)

O painel baker está dividido em 4 partes:

### 1: Cena

![](bakers-legacy-interface.resources/image2017-3-13-9-35-53.png)

Permite definir qual parte da malha está envolvida no processo de fça bake.

Novo na versão 6, você também pode selecionar por material:

![](bakers-legacy-interface.resources/image2017-3-13-9-45-26.png)

### 2: Baker

![](bakers-legacy-interface.resources/image2017-3-13-9-46-26.png)

Pressionando o botão ![](bakers-legacy-interface.resources/image2017-3-13-9-47-47.png), você pode adicionar os baker desejados à lista de processamento

>[!NOTE]
>
> Os padings são processados seguindo a ordem da lista (de cima para baixo): isso pode ser importante se você quiser reutilizar o resultado de um faço bake (como o mapa normal) em outro processo de fça bake

Clicar no “+” no layout baker permite adicionar os baker em uma pilha (Você pode colocar quantos baker quiser em uma pilha).

.![](bakers-legacy-interface.resources/image2017-3-13-9-52-8.png)

Você pode remover um processo de fça bake da lista pressionando ![](bakers-legacy-interface.resources/image2017-3-13-9-54-33.png)

Você pode reordenar a lista de processos de fça bake selecionando um processo de fça bake e usando ![](bakers-legacy-interface.resources/image2017-3-13-9-55-33.png)

### 3: parâmetros de Baker

![](bakers-legacy-interface.resources/image2017-3-13-13-24-0.png)

Esta seção exibe as opções específicas para o baker selecionado atualmente.

### 4: Parâmetros Comuns

![](bakers-legacy-interface.resources/image2017-3-13-13-28-12.png)

Exibe os parâmetros compartilhados entre baker.

>[!NOTE]
>
> Por default, alterar um desses parâmetros afetará todos os baker, exceto se você marcar Sobrepor Parâmetros, comum a todos os baker: nesse caso, as alterações serão locais para o baker atual.

* O campo **Nome do Recurso** permite alterar o nome do bitmap gerado, se desejado.
* A lista suspensa **Formato de Arquivo** permite alterar o formato de arquivo do padrão (formato de Bitmap do Windows ou OS/2, “BMP”).
* **A caixa de seleção** **Colocar** recurso em uma pasta específica de malha permite escolher se o bitmap gerado será armazenado no mesmo nível que o modelo ou dentro de uma nova subpasta denominada “Recursos”.
* **O Método** permite definir se o novo recurso de bitmap deve ser vinculado ou incorporado no pacote de Substance.
* **A pasta** permite definir onde salvar os mapas.

Pressionar o botão OK no canto inferior direito da janela baker iniciará o processo de fça bake.

Novo na versão 6: agora você pode cancelar o processo de fça bake com o botão Cancelar:

![](bakers-legacy-interface.resources/image2017-3-13-13-50-4.png)
