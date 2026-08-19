---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/visible-if-control-visibility-of-inputs-outputs-and-parameters.html"
breadcrumb-title: ''
description: Saiba como usar expressões if visíveis no Substance 3D Designer para controlar a visibilidade de parâmetros com base em condições.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Visible if expressions
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Visível se expressões
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1511dc8cc9a91529359172ad81cd2c1c0606448f
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 1%

---


# Visível se expressões

A expressão &#39;Visible if&#39; permite que você <b>controle a visibilidade</b> de entradas, saídas e parâmetros em gráficos.

Ao [expor parâmetros](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), talvez você queira ocultar ou mostrar parâmetros ou conectores de nó com base no status de outros parâmetros. Por exemplo, um controle deslizante é exibido somente quando um botão de parâmetro booleano está definido como `true`, pois caso contrário ele não teria efeito e isso pode confundir os usuários.

Para isso, você pode inserir uma *expressão lógica* na propriedade <b>Visible if</b> de:

* o [parâmetro de entrada](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) de um gráfico;
* nó [de entrada](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) de um gráfico;
* nó [de saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) de um gráfico.

![Alternando a visibilidade do parâmetro de entrada](../../assets/visible-if-example.gif "Alternando a visibilidade do parâmetro de entrada"){width="512px"}

Se a expressão lógica for avaliada como `true`, o parâmetro, a entrada ou a saída será exibido em todos os [nós de instância](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) que representam o gráfico atual. Caso contrário, ele será *oculto*.

Condições complexas são possíveis, desde que a expressão lógica indicando essas condições seja válida.

>[!NOTE]
>
> Advertências
> 
> * Este recurso *somente* afeta o fato de um parâmetro ou conector ser exibido na interface do usuário e não ter *nenhum efeito* sobre os cálculos e o resultado de um gráfico.
> * Ao expor ou aplicar uma função a qualquer parâmetro usado em instruções &#39;Visible if&#39;, essas instruções serão *ignoradas* e o padrão será &#39;true&#39;.

>[!IMPORTANT]
>
> Embora essa funcionalidade funcione dentro do ecossistema do Substance 3D, algumas integrações podem não oferecer suporte a ela. Se não houver suporte, a condição de visibilidade assumirá `true` como padrão.

## Escrever expressões &#39;Visible if&#39;

### ACESSANDO PARÂMETROS DE ENTRADA

Qualquer expressão If visível precisará usar pelo menos uma entrada, isso pode ser feito por meio da seguinte sintaxe:

```
input.identifier 

input["identifier"]
```


>[!WARNING]
>
> O **identificador** deve ser o nome *exato* da propriedade **Identificador** de um parâmetro de entrada existente e deve ser digitado *com distinção entre maiúsculas e minúsculas*. Você *não pode* fazer referência a um parâmetro por seu Rótulo.\
>  Se um parâmetro referenciado não existir ou a expressão lógica for inválida, um *aviso* será exibido na propriedade **Visible if**.

### OPERADORES DISPONÍVEIS

Os campos “Visible if” aceitam os seguintes parâmetros:

* Entradas booleanas, flutuantes e inteiras.
* `true` e `false` valores (diferencia maiúsculas de minúsculas, sem maiúsculas!)
* `.x` : acessar o subparâmetro
* `&&`<b> </b>: e
* `||`<b> </b>: ou
* `!`<b> </b>: não
* `<`<b>, </b>`>`<b>, </b>`<=`<b>, </b>`>=`<b>, </b>`==`<b>, </b>`!=` : comparação
* `()` : colchetes

### DEVE SEMPRE AVALIAR PARA BOOLEANOS

Uma Expressão If Visível é usada como condição para uma instrução “IF”, o que significa que sempre deve resultar em `true` ou `false`.

* Valores boolianos podem ser avaliados diretamente como a condição. Um botão simples com um valor booleano não requer mais do que isso. Ver exemplos infra, primeiro caso;
* Parâmetros não booleanos geralmente requerem uma operação *comparação*. Veja acima para operadores de comparação, abaixo para exemplos;
* Alguns valores não booleanos podem ser *verdadeiros* ou *falsos*, o que significa que podem ser avaliados como `true` de `false` - Por exemplo. um valor inteiro de `0` é avaliado como false.

## Exemplos

| Condição (”If”) | Fórmula | Nota |
| --- | --- | --- |
| Verdadeiro | ` input["my_input"]   input.my_input `  ` input["my_input"] == true   input.my_input == true ` | my\_input é um valor booliano |
| Falso | ` !input["my_input"]   !input.my_input `  ` input["my_input"] == false   input.my_input == false `  ` input["my_input"] != true   input.my_input != true ` | my\_input é um valor booliano |
| Inferior a | ` input["my_input"] < 3   input.my_input < 3 ` | my\_input é um valor inteiro |
| Igual | ` input["param1"] == 2   input.param1 == 2 ` | param1 é um valor float ou inteiro |
| Inferior a | ` input["my_input"].y < 3   input.my_input.y < 3 ` | my\_input é um valor float ou inteiro com um ou mais componentes - por exemplo, float2(x, y), integer3(x, y, z) |
| Ou | ` input["param1"] \|\| input["param2"]   input.param1 \|\| input.param2 ` | param1 e param2 são valores booleanos |
| E | ` input["param1"] > 0 && input["param2"] > 1   input.param1 > 0 && input.param2 > 1 ` | param1 e param2 são valores float ou integer |
