---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs/variables/create-a-variable.html"
breadcrumb-title: ''
description: Saiba como criar variáveis personalizadas nos gráficos de função do Substance 3D Designer para valores e parâmetros reutilizáveis.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Create a variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Criar uma variável
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# Criar uma variável

Há diferentes maneiras de criar uma variável no Substance 3D Designer:

* Uso de um parâmetro de entrada
* Use um nó Set.

## Uso de um parâmetro de entrada

Quando você cria um parâmetro de entrada, uma variável é criada e associada a ela. Em seguida, é possível reutilizar essa variável em qualquer função do gráfico.

Portanto, um único parâmetro exposto pode influenciar várias partes do seu gráfico.

## Usando um nó Set

Um nó Set é um nó disponível apenas nos gráficos de função:

Permite que o usuário crie uma variável personalizada:

* O nome é declarado nos parâmetros.
* O valor é definido pela entrada.

### Como usar o nó *Conjunto*

O uso de um nó Set é um pouco específico:

ao declará-lo, ele fica disponível apenas no gráfico, o que, por padrão, não é muito útil (afinal, já é possível gerar o valor com links).

Portanto, você tem que declarar esta nova variável, fora deste gráfico.

para fazer isso, use um nó de sequência e execute as seguintes etapas:

* Vincule o nó de saída real à “última” entrada do nó de sequência
* Vincule o nó Set à entrada “In” do nó de sequência.
* Definir a sequência como o nó de saída

Quando você tiver feito isso, a variável estará disponível no outro gráfico de função do mesmo nó.

>[!WARNING]
>
> Quando um nó é processado pelo engine substance, seus parâmetros (e as funções que poderiam controlá-los) são lidos de cima para baixo. Portanto, um nó Set só pode ser acessível pelos parâmetros localizados abaixo dele na pilha de parâmetros do nó.

>[!NOTE]
>
> Se você tiver várias variáveis para criar, basta repetir a operação de criação dos nós *Conjunto* e *Sequência* e definir o último nó de sequência como o nó de saída:
> 
> ![](create-a-variable.resources/create-a-variable-01.png)
