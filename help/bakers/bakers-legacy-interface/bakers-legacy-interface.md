---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: Saiba mais sobre a interface herdada dos padeiros da Substance 3D Designer para usuários familiarizados com versões mais antigas.
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Interface herdada de padarias
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 3%

---


# Interface herdada de padarias

Esta é a descrição da interface de panificação disponível nas versões do [Adobe Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html) anteriores à 6.0.4.

## Visão geral

![](../../assets/image2017-3-13-9-33-40.png)

O painel do padeiro divide-se em 4 partes:

### 1: Cena

![](../../assets/image2017-3-13-9-35-53.png)

Permite definir qual parte da malha está envolvida no processo de cozimento.

Novo na versão 6, você também pode selecionar por material:

![](../../assets/image2017-3-13-9-45-26.png)

### 2: Padarias

![](../../assets/image2017-3-13-9-46-26.png)

Pressionando o botão ![](../../assets/image2017-3-13-9-47-47.png), você pode adicionar os preparadores desejados à lista de processamento

>[!NOTE]
>
> Os cozidos são processados seguindo a ordem da lista (de cima para baixo): isso pode ser importante se você quiser reutilizar o resultado de um cozido (como o mapa normal) em outro processo de cozimento

Clicar no “+” no layout de padeiros permite adicionar os padeiros em uma pilha (Você pode colocar quantos padeiros quiser em uma pilha).

.![](../../assets/image2017-3-13-9-52-8.png)

Você pode remover um processo de cozimento da lista pressionando ![](../../assets/image2017-3-13-9-54-33.png)

Você pode reordenar a lista de processos de cozimento selecionando um processo de cozimento e usando ![](../../assets/image2017-3-13-9-55-33.png)

### 3: Parâmetros de padeiros

![](../../assets/image2017-3-13-13-24-0.png)

Esta seção exibe as opções específicas para o padeiro atualmente selecionado.

### 4: Parâmetros Comuns

![](../../assets/image2017-3-13-13-28-12.png)

Exibe os parâmetros que são compartilhados entre padeiros.

>[!NOTE]
>
> Por padrão, alterar um desses parâmetros afetará todos os padeiros, exceto se você marcar Substituir parâmetros, comuns a todos os padeiros: nesse caso, as alterações serão locais para o padeiro atual.

* O campo **Nome do Recurso** permite alterar o nome do bitmap gerado, se desejado.
* A lista suspensa **Formato de Arquivo** permite alterar o formato de arquivo do padrão (formato de Bitmap do Windows ou OS/2, “BMP”).
* **A caixa de seleção** **Colocar** recurso em uma pasta específica de malha permite escolher se o bitmap gerado será armazenado no mesmo nível que o modelo ou dentro de uma nova subpasta denominada “Recursos”.
* **O Método** permite definir se o novo recurso de bitmap deve ser vinculado ou incorporado no pacote de Substance.
* **A pasta** permite definir onde salvar os mapas.

Pressionar o botão OK na parte inferior direita da janela de padaria iniciará o processo de cozimento.

Novo na versão 6: agora você pode cancelar o processo de cozimento com o botão cancelar:

![](../../assets/image2017-3-13-13-50-4.png)
