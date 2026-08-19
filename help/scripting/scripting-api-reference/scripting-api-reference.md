---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/scripting/scripting-api-reference.html"
breadcrumb-title: ''
description: Acesse a referência completa da API de script Python do Substance 3D Designer para desenvolvimento de plug-ins.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Scripting API reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Referência da API de script
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 0%

---


# Referência da API de script

Esta página descreve os principais conceitos da API.

Para obter informações mais detalhadas, consulte a documentação que acompanha o aplicativo que está acessível em <b>Ajuda > Documentação da API Python...</b>. Nesta documentação, faça uma <b>Pesquisa rápida</b> para os nomes de módulos (entre parênteses abaixo) para encontrar facilmente sua definição.

## Contexto

O objeto de contexto (*Contexto*) é o <b>ponto de entrada principal para a API</b>. É criado na primeira vez que o usuário o obtém usando o método &#39;<b>*getContext()*</b>&#39; do módulo &#39;*sd*&#39;.

Este objeto permite essencialmente <b>recuperar o objeto de aplicativo</b> (*SDApplication*).

## Aplicativo (SDApplication)

O aplicativo (*SDApplication*) é o objeto que permite o <b>acesso aos principais gerenciadores de API</b>, como:

* o <b>Gerenciador do Pacote </b> (*SDPackageMgr*) que gerencia todos os <b>pacotes</b> do aplicativo;
* o <b>Gerenciador do </b>Módulo (*SDModuleMgr*) que gerencia todos os <b>módulos</b> do aplicativo;
* o <b>Gerente de IU </b> (*SDUIMgr*) que pode criar <b>menus e docks</b> na janela do aplicativo.

Você pode registrar <b>retornos de chamada</b> com o aplicativo que será chamado quando determinados eventos ocorrerem.

## Gerenciador de Pacotes (SDPackageMgr)

Este objeto gerencia todos os <b>pacotes</b> do aplicativo. Os pacotes são exibidos no componente &#39;<b>*Explorer*</b>&#39;.

Ele permite:

* <b>criar</b> um novo pacote;
* <b>carregar/descarregar</b> um pacote;
* <b>salvar</b> um pacote;
* <b>encontre</b> um pacote.

## Pacote (SDPackage)

Um pacote (*SDPackage*) é uma <b>coleção de recursos</b> (*SDResource*).

O conteúdo de um pacote pode ser <b>armazenado</b> em um arquivo com a extensão <b>.sbs</b> por meio do objeto &#39;*SDPackageMgr*&#39;. Este objeto permite que você <b>recupere </b>recursos específicos.

Para <b>criar</b> um recurso específico, consulte os métodos estáticos de objeto relacionados (por exemplo: &#39;*SDSBSCompGraph.sNew()*&#39;).

Um pacote também contém um dicionário de metadados (SDMetadataDict). Você pode encontrar mais informações sobre metadados [aqui](../../package-metadata/package-metadata.md).

## Recurso (SDResource)

Um recurso (*SDResource*) é um objeto que pode ser <b>referenciado</b> por outro recurso.

Há vários <b>tipos</b> de recursos:

* Pastas (*SDResourceFolder*);
* Gráficos (*SDGraph*);
* Bitmaps (*SDResourceBitmap*);
* Imagens SVG (*SDResourceSVG*);
* Fontes (*SDResourceFont*);
* Cenas (*SDResourceScene*);
* Medições BSDF (*SDResourceBSDFMeasurement*);
* Perfis Light (*SDResourceLightProfile*).

Um recurso pode ser <b>criado</b> do método estático &#39;*sNew()*&#39; em:

* uma viagem organizada;
* uma pasta.

Um recurso pode ter várias <b>propriedades</b> (*SDProperty*).

## Gerenciador de interface de usuário (SDUIMgr)

O gerenciador de interface de usuário permite <b>criar elementos de interface de usuário</b> na janela principal do Substance Designer, como <b>menus</b>, <b>docks</b>, e permite registrar <b>retornos de chamada</b> quando ocorrerem eventos relacionados à interface de usuário.

Além disso, o gerenciador de interface do usuário tem acesso ao <b>gráfico ativo atual</b> e à <b>seleção</b> do gráfico ativo.

## Gráficos (SDGraph)

Um gráfico (*SDGraph*) é um objeto que contém:

* <b>nós </b>(*SDNode*);
* <b>objetos de gráfico</b> (*SDGraphObjects*);
* <b>propriedades </b>(*SDProperty*).

Existem 4 tipos diferentes de gráficos:

* Gráfico de Substance (*SDSBSCompGraph*)
* Gráfico de função de Substance (*SDSBSFunctionGraph*)
* Gráfico Substance FXMap (*SDSBSFxMapGraph*)

Um gráfico pode ter um ou vários nós de <b>saída</b>. Os nós de saída representam os <b>resultados</b> do gráfico.

Todos os nós disponíveis para um gráfico podem ser <b>recuperados</b> com o método &#39;*getNodeDefinitions()*&#39;.

Um novo nó pode ser <b>criado</b> com o método &#39;*newNode()*&#39;.

Um novo nó <b>instância</b> pode ser criado a partir de um recurso (*SDResource*) com o método &#39;*newInstanceNode()*&#39;.

## Nó (SDNode)

Um nó (*SDNode*) representa uma <b>operação</b> realizada em um objeto.

Ele pode ser criado a partir de:

* uma <b>definição</b> (*SDDefinition*) (consulte &#39;*SDGraph.newNode()&#39;*);
* um <b>recurso</b> (*SDResource*) (consulte &#39;*SDGraph.newInstanceNode()&#39;*).

Um nó pode ter várias <b>propriedades</b>.

Há vários <b>tipos</b> de nó:

* *<b>SDSBSCompNode</b>*: um nó do Gráfico do Substance (*SDSBSCompGraph*);
* *<b>SDSBSFunctionNode</b>*: um nó do Gráfico de função do Substance (*SDSBSFunctionGraph*);
* *<b>SDSBSFxMapNode</b>*: um nó do gráfico Substance FXMap (*SDSBSFxMapGraph*);

## Objetos de gráfico (SDGraphObjects)

Um objeto de gráfico (*SDGraphObject*) é um objeto que <b>adiciona informações adicionais</b> ao gráfico, mas que <b>*não* é levado em consideração</b> durante o processo de avaliação do gráfico.

Há <b>3 tipos</b> de objetos de gráfico:

* <b>Pin</b> (*SDGraphObjectPin*)
* <b>Comentário</b> (*SDGraphObjectComment*)
* <b>Quadro</b> (*SDGraphObjectFrame*)

Consulte o método estático &#39;*sNew()*&#39; nesses objetos para obter mais informações sobre como <b>criá-los</b>.

## Propriedades (SDProperty)

Uma propriedade (*SDProperty*) é um objeto que <b>descreve</b> uma propriedade de <b>outro objeto</b> (um gráfico, um nó, um recurso etc.).

Pertence a uma <b>categoria</b> específica (*SDPropertyCategory*):

* <b>Entrada</b>: classifica as propriedades de entrada de um objeto, que geralmente<b> afetam a operação</b> realizada pelo objeto atual;
  * Por exemplo: a propriedade &#39;*color*&#39; de um nó de Cor Uniforme em um gráfico de Substance é uma propriedade de entrada;
* <b>Saída</b>: classifica as propriedades de saída de um objeto. É usado para identificar um <b>resultado</b> de um objeto;
* <b>Anotação</b>: classifica propriedades que <b>*não* afetam a operação</b> realizada por um objeto;
  * Exemplo: o &#39;*rótulo*&#39; de um gráfico é uma propriedade de anotação, pois não afeta o cálculo do gráfico.

Contém os <b>membros</b> a seguir:

* <b>Id</b>: o identificador da propriedade no contexto desta categoria;
* <b>Tipos</b>: os tipos suportados pela propriedade atual. Algumas propriedades podem suportar *vários* tipos: &#39;*int*&#39;, &#39;*float*&#39;, etc.;
  * Ex: as propriedades de entrada de um nó &#39;*sbs::function::add*&#39; podem suportar tipos diferentes: &#39;*int&#39;*, &#39;*int2&#39;*, &#39;*int3&#39;*, &#39;*int4&#39;*, &#39;*float&#39;*, &#39;*float2&#39;*, &#39;*float3&#39;*, &#39;*float4&#39;, etc.;*
* <b>Categoria</b>: a categoria à qual a propriedade pertence (entrada, saída, anotação);
* <b>Rótulo</b>: o rótulo da propriedade, usado para exibição *somente*;
* <b>Descrição</b>: a descrição da propriedade;
* <b>DefaultValue</b>: O valor padrão;
* <b>IsConnectable</b>: indica se uma conexão (*SDConnection*) *pode* ser realizada nesta propriedade;
* <b>isReadyOnly</b>: indica se a propriedade é somente leitura. Se for true, o valor associado a ele *não* poderá ser modificado;
* <b>isVariadic</b>: se for true, esta propriedade será representada como *várias* propriedades no objeto;
* <b>isPrimary</b>: indica se a propriedade especificada é a propriedade *principal* que controla algumas outras propriedades. *Observação:* isto é específico para nós de Substance *Composição* (*SDSBSCompNode*)).

Exemplos:

* Propriedades do nó &#39;*sbs::compositing::input*&#39;:

<table data-preserve-html="true"><colgroup><col style="width: 276.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::input</th></tr><tr><td style="text-align: left;"><strong>Entrada</strong></td><td style="text-align: left;"><strong>Anotação</strong></td><td style="text-align: left;"><strong>Saída</strong></td></tr><tr><td>$outputsize</td><td>rótulo</td><td><p>unique_filter_output (CONNECTABLE)</p></td></tr><tr><td>$format</td><td>descrição</td><td><br/></td></tr><tr><td>$pixelsize</td><td>identificador</td><td><br/></td></tr><tr><td>$pixelratio</td><td>userdata</td><td><br/></td></tr><tr><td>$tiling</td><td>grupo</td><td><br/></td></tr><tr><td>$randomseed</td><td>visibleif</td><td><br/></td></tr><tr><td><p>bitmapresourcepath</p></td><td>usos</td><td><br/></td></tr></tbody></table>

* Propriedades do nó &#39;*sbs::compositing::blend*&#39;:

<table data-preserve-html="true"><colgroup><col style="width: 278.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::blend</th></tr><tr><td style="text-align: left;"><strong>Entrada</strong></td><td style="text-align: left;"><strong>Anotação</strong></td><td style="text-align: left;"><strong>Saída</strong></td></tr><tr><td>$outputsize</td><td><br/></td><td>unique_filter_output (CONNECTABLE)</td></tr><tr><td>$format</td><td><br/></td><td><br/></td></tr><tr><td>$pixelsize</td><td><br/></td><td><br/></td></tr><tr><td>$pixelratio</td><td><br/></td><td><br/></td></tr><tr><td>$tiling</td><td><br/></td><td><br/></td></tr><tr><td>$randomseed</td><td><br/></td><td><br/></td></tr><tr><td>source.connector (CONNECTABLE)</td><td><br/></td><td><br/></td></tr><tr><td><p>destination.connector (CONNECTABLE)</p></td><td><br/></td><td><br/></td></tr><tr><td>opacity.connector (CONNECTABLE)</td><td><br/></td><td><br/></td></tr><tr><td>opacitymult</td><td><br/></td><td><br/></td></tr><tr><td colspan="1">blendingmode</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">colorblending</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">maskretangle</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr></tbody></table>

## Tipo (SDType)

Um tipo (*SDType*) contém informações de um valor <b>tipo</b>, como:

* <b>Id</b>: o identificador do tipo;
* <b>Modificador</b>: o modificador de tipo que pode ser um dos valores &#39;*SDTypeModifier&#39;* <b>enum</b>:
  * *Automático*;
  * *Uniforme*: o valor é avaliado *uma vez* por operação;
  * *Variável*: o valor é avaliado *várias vezes* por operação (por exemplo, para cada texel).

Vários tipos são definidos, como:

* <b>enums</b> (*SDTypeEnum*): descreve um tipo <b>enumeração</b> com todas as suas propriedades;
* <b>estruturas</b> (*SDTypeStruct*): descreve um tipo <b>estrutura</b> com todas as suas propriedades;
* <b>matriz</b> (*SDTypeArray*): descreve uma <b>matriz</b>.
* etc.

Consulte *Documentação da API Python* para ver uma lista completa.

## Valores (SDValue)

Um valor (*SDValue*) é um objeto que <b>encapsula</b> um valor de *tipo base*.

Por exemplo:

* um objeto &#39;<b>*SDValueInt*</b>&#39; encapsula um valor &#39;*int*&#39;;
* um objeto &#39;<b>*SDValueFloat4*</b>&#39; encapsula um valor &#39;*float4*&#39;;
* etc.

O valor do tipo base geralmente pode ser <b>recuperado</b> com o método &#39;<b>get()</b>&#39;, mas isso pode depender do *tipo* de &#39;*SDValue&#39;* que foi retornado.

## Conexão (SDConnection)

Uma conexão (*SDConnection*) representa um <b>link</b> entre duas propriedades<b> diferentes</b> de dois <b>nós</b> diferentes.

Contém:

* O <b>nó de destino</b>;
* A <b>propriedade de destino</b> do nó de destino;

Todas as <b>operações de conexão</b> são executadas em um nó:

* <b>criando</b> uma nova conexão, consulte &#39;*SDNode.newPropertyConnection()*&#39;
* <b>excluindo</b> uma conexão existente, consulte &#39;*SDNode.deletePropertyConnection()*&#39;
* <b>recuperando</b> as conexões de uma propriedade, consulte &#39;*SDNode.getPropertyConnections()*&#39;

## Módulo (SDModule)

Um módulo é uma <b>coleção de definições e tipos</b>.

Ele permite uma fácil recuperação de todas as informações sobre os nós que podem ser criados, bem como sobre enumerações e estruturas.

Contém:

* um <b>identificador</b> (*Id*) exclusivo no contexto do gerenciador de módulo (*SDModuleMgr*);
* uma lista de <b>definições</b> (*SDDefinition*);
* uma lista de <b>tipos</b> (*TipoDT*).

## Definição (SDDefinition)

Um objeto de definição (*SDDefinition*) contém informações sobre a definição de um <b>objeto</b> específico com base nas <b>propriedades</b> (&#39;*SDNode&#39;* etc.).

Contém:

* <b>Id</b>: o identificador da definição;
* <b>Rótulo</b>: o rótulo da definição;
* <b>Descrição</b>: a descrição da definição;
* <b>Propriedades</b>: as propriedades de todas as *categorias* de propriedade disponíveis (*SDPropertyCategory*).
