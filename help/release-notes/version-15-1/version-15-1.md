---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-15-1.html"
breadcrumb-title: ''
description: Consulte as notas de versão do Substance 3D Designer versão 15.1 para saber mais sobre novos recursos, aprimoramentos e correções de erros.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 15.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versão 15.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1719'
ht-degree: 0%

---


# Versão 15.1

O Substance Designer 15.1 traz uma janela de criação de gráficos completamente renovada com acesso direto à amostra, nós de ruído aprimorados para maiores possibilidades criativas, categorias organizadas no menu do nó e muito mais.

*Data de lançamento: 11 de dezembro de 2025*

![Banner do Designer 15.1](../../assets/bannerweb.png)

## Aprimorar criação de gráfico

Nesta versão, a [janela de criação de gráficos](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) foi <b>amplamente redesenhada</b> para aprimorar a experiência inicial do usuário no Substance 3D Designer. O principal objetivo desta atualização é simplificar o processo de seleção de modelos, permitindo que os usuários identifiquem com eficiência o modelo mais adequado para seus requisitos.

As miniaturas oferecem <b>referências visuais</b> instantâneas para os tipos de material pretendidos, enquanto as dicas de ferramentas detalhadas fornecem todas as informações pertinentes. Para melhorar a organização, os modelos agora são classificados em <b>categorias</b> específicas, como materiais, filtros e processamento de digitalização.

Embora a interface principal tenha sido atualizada, os usuários continuam a ter acesso a exibições anteriores, incluindo opções de lista, pacotes e diretórios.

[Saiba mais](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)

![redesenhar nova janela de gráfico](../../assets/newgraph.png){zoomable="yes"}

## Amostras incorporadas

Com o lançamento de nossa janela de criação de gráficos redesenhada, adicionamos uma variedade de [<b>materiais de amostra</b>](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md) diretamente no software. Esse aprimoramento é uma resposta à sua solicitação de melhor acesso aos recursos de aprendizado.

![Nova janela de criação de gráfico para amostras](../../assets/GraphSample.png){zoomable="yes"}

Para atender a essa necessidade, incluímos amostras de materiais, como tecidos (incluindo couro e cetim), madeira, metal, plástico, cerâmica e muito mais. Esses exemplos têm como objetivo ajudar você a iniciar seus projetos com facilidade e se familiarizar com os nós da família principal disponíveis no Substance 3D Designer

Cada gráfico é <b>anotado</b>, cuidadosamente organizado e contém um número mínimo de nós para torná-lo o mais fácil de entender possível.

Você pode acessar as amostras na categoria “Amostras de materiais” ao criar um novo gráfico de Substance ou diretamente na tela inicial usando o conveniente botão “Ir para amostras”.

Juntamente com esses materiais fundamentais, também fornecemos <b>amostras avançadas</b> para demonstrar como usar os recursos do <b>FX-map e do processador de pixels</b> de maneira mais eficaz.

[Saiba mais](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md)

![amostra de madeira no substance designer](../../assets/samplegraph.png){zoomable="yes"}

## Novos ruídos

Os ruídos desempenham um papel crucial na maioria dos gráficos, e é por isso que nos concentramos em vários aprimoramentos importantes nesta versão para melhorar sua funcionalidade e usabilidade.

Com esta atualização, introduzimos <b>melhor suporte para cenários sem divisão em blocos gráficos</b>, garantindo que os padrões de ruído se comportem como esperado sem a divisão em blocos obrigatória. Anteriormente, os nós de ruído eram forçados a dividir em blocos gráficos ou produziam resultados incorretos quando a divisão em blocos gráficos estava desativada.

A maioria dos ruídos agora inclui <b>novos parâmetros</b>, fornecendo aos usuários maior controle criativo. Essas opções adicionais permitem que os autores de gráficos ajustem a aparência e o comportamento do ruído em seus fluxos de trabalho.

Finalmente, a profundidade de bits <b>não está mais bloqueada para 16 bits</b>. Agora, você pode substituir a configuração de profundidade de bits em instâncias de nós individuais, permitindo obter detalhes mais altos e um intervalo dinâmico quando necessário, ou otimizar seus gráficos para obter desempenho.

Veja a lista completa de ruídos atualizados nas [notas de versão](#release-notes) abaixo.

Exemplos: [Células 1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md) [Nuvens 2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-2/clouds-2.md) [Arranhões direcionais](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-scratches/directional-scratches.md) [Ruído de umidade 1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise/moisture-noise.md)

![ruído de distúrbio direcional](../../assets/directionaldisorder.gif){zoomable="yes"}

## Hierarquia no menu do nó

Para enfrentar o desafio de localizar nós específicos dentro da extensa biblioteca, introduzimos categorias no menu Nó.

O grande número de nós disponíveis pode dificultar a localização rápida do nó desejado. Para simplificar este processo, um novo atributo [<b>Grupo</b>](../../compositing-graphs/graph-parameters/graph-parameters.md) foi implementado no nível de gráfico. Quando este atributo é definido, ele é usado para organizar e classificar os resultados da pesquisa.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Pesquisa de ![nó com categoria 1](../../assets/search1-2.png){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

Pesquisa de ![nó com categoria 2](../../assets/search2.png){zoomable="yes"}

</td>
</tr>
</table>

## Saída padrão

Quando um nó tem várias [saídas](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), não é possível exibir todas elas simultaneamente na exibição 2D ou como a miniatura do nó. A diretriz predominante em tais cenários é utilizar o primeiro pino conectado ou, se nenhum estiver conectado, a primeira saída por padrão.

No entanto, essa abordagem nem sempre pode produzir resultados ideais. Por exemplo, em alguns nós de spline, o primeiro pino conectado geralmente representa os dados de coordenadas de spline, o que não é adequado para fins de visualização.

Para resolver isso, um atributo de saída padrão foi introduzido. Este recurso permite que o autor do gráfico <b>especifique qual saída deve ser exibida por padrão</b>, aprimorando assim a intuitividade do uso do nó e facilitando uma compreensão mais clara do gráfico criado.

Experimente a imagem abaixo para ver a diferença antes e depois da definição de saída padrão.

[Saiba mais](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

<table>
  <tr>
    <td>
      <img src="../../assets/defaultouput2.png" alt="defaultouput2">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../assets/defaultouput1.png" alt="Com a saída padrão, as miniaturas são sempre relevantes.">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

## Nó &#39;Está definido&#39;

Ao trabalhar com gráficos de função, talvez seja necessário determinar se uma [variável](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) existe no gráfico.

Por exemplo, detectar a ausência de uma variável permite fornecer um valor de fallback, garantindo que a função se comporte como esperado sem exigir que cada entrada seja definida explicitamente. Por isso adicionamos o nó [&#39;Está definido&#39;](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md).

[Saiba mais](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)

![Nó definido](../../assets/isdefined.png){zoomable="yes"}

## Notas de versão

### 15.1.0

*(Lançado em 11 de dezembro de 2025)*

### Adicionado

* [NewGraph] Retrabalho da janela do novo gráfico
* [NewGraph] Adicione amostras de materiais e amostras avançadas
* [NewGraph] Adiciona um novo atributo para o gráfico para os dados do modelo (categoria e subtítulo)
* [NewGraph] Remover opção de formato de saída
* [Conteúdo] Adicionar funções de hash
* [Content] Adicionar mapeadores de tons a functions.sbs
* [Content] Ruído anisotrópico v2: adicionar formato de saída padrão, adicionar distúrbio
* [Content] Aplique capitalização de sentença a rótulos de nó e parâmetros
* [Content] BnW spots 1 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] BnW spots 2 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] BnW spots 3 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Células 1, 2, 3, 4 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos, opções de desordem
* [Content] Nuvens 1 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Nuvens 2 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Nuvens 3 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Conteúdo] Cor para mascarar v2
* [Content] Ruído direcional 1 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Ruído direcional 2 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Ruído direcional 3 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Ruído direcional 4 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Arranhões direcionais v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Dirt 1 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Dirt 2 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Dirt 3 v2: adicionar formato de saída padrão, sem suporte a divisão em blocos gráficos
* [Content] Dirt 4 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Dirt 5 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Conteúdo] Degradê de Dirt v2: adicionar formato de saída padrão, novas opções de doença
* [Content] Soma fractal Base v2: adicionar formato de saída padrão, distúrbio, sem suporte a divisão em blocos gráficos
* [Content] Soma fractal 1, 2, 3, 4 v2: adicionar formato de saída padrão
* [Content] Ruído gaussiano v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Manchas gaussianas 1 e 2 v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Content] Messy fiber 1,2,3 v2: adicionar formato de saída padrão, sem suporte a azulejos, opções de desordem
* [Content] Ruído por umidade v2: adicionar formato de saída padrão, sem suporte para revestimento
* [Content] Novo nó “Umidade noise 2”
* [Content] Ruídos: atualize para adicionar um formato de saída padrão
* [Content] Perlin noise v2: adicionar formato de saída padrão, sem suporte para divisão em blocos gráficos
* [Conteúdo] Mapeador de formas: adicionar modo de filtragem
* [Content] Mapeador UV: adicionar modo de filtragem
* [Content] Forma de onda 1 v2: usar formato de saída padrão + novas opções
* [Content] White noise v2: usar formato de saída padrão, adicionar opções de distribuição
* [Padeiros] Exibir os UVs somente da malha selecionada
* [Padeiros] Adicione uma opção para selecionar o método de correspondência de geometria por nome
* [Padeiros] Selecione o Padeiro mais próximo quando um padeiro é excluído
* [Padarias] UDIM: defina uma lista de blocos UV para assar
* [Bakers] Atualize o bake sdk para 3.15.4
* [3D View/SceneBrowser] Evite selecionar um UsdPrimitive ao fazer um clique com o botão direito nele
* [ColorManagement] Suporte para ACES 2.0
* [Gráfico de composição] Permite definir um nó de saída como a “Saída padrão”
* [Fogão] Remover aviso sobre entradas desconectadas de instâncias de função¬†
* [Funções] Adicionar operador isDefined
* [Graph] Agrupar os itens por atributo &#39;group&#39; no menu do nó
* [Gráfico] Melhorar a renderização de miniaturas

### Correções

* [3D View] A textura da Escala de cinza L16 é exibida com uma tonalidade vermelha quando conectada ao ambiente ou à baseColor
* [Exibição 3D] Alterar a vinculação de material de uma cena sem material cria um novo material “padrão”
* [3D View] As normais computadas não são corretas para malhas OBJ específicas
* [Exibição 3D] O ambiente personalizado de SBSSCN não é visível no carregamento no Pathtracer
* [Visualização 3D] Erros no console ao girar um ambiente desativado
* [Exibição 3D] O Specular level não foi aplicado corretamente
* [Exibição 3D] O Specular edge color não funciona ao usar o rasterizador de Eclair
* [Exibição 3D] O material adicionado do usuário não é aplicado em cenas padrão
* [3D View]&#x200B;[Padarias] A cor do material fica muito escura depois de substituída ou ao usar um padeiro “Colorido”
* [Exibição 3D]&#x200B;[Padeiros] Sem cor material do arquivo FBX
* [Padeiros] As cores do material em arquivos FBX não são detectadas corretamente
* [Bakers] A opção &#39;recompute\_tangents&#39; é sempre &#39;false&#39; nas exportações predefinidas JSON
* [Bakers] CLI: Falha ao executar o mesmo panificador consecutivamente através do arquivo JSON
* [Padeiros] A atualização do parâmetro &#39;color-generator&#39; não funciona para &#39;Grayscale&#39;
* [Conteúdo] Máscara para caminhos: falha em proporções não quadradas
* [Content] Renderizador de Renderização PBR/ícone: função incorreta do lobo de specular
* [Content] Caminhos para spline: defina o “Tamanho de saída” como “Em relação ao pai” por padrão
* [Content] Lista de pontos: os pontos não estão na ordem correta quando a textura dos dados é não quadrada
* [Content] Mapeador de spline: falha de linha de 1 px em casos aleatórios
* [Content] Mapeador de spline: UVs esticados em alguns casos quando o thickness é 0
* [Graph] Falha ao excluir a saída de um subgrafo de função
* [Graph] O tipo de cor do nó de entrada pode ser alterado em pacotes somente leitura
* [Graph] A entrada principal pode ser alterada em pacotes somente leitura
* [Propriedades] A cor do widget de visualização de cor não corresponde ao estado do botão sRGB
* [Cena] Não é possível carregar um arquivo OBJ maior que 2 GB
* [IU] Os estados de encaixe do console e do gerenciador de dependências não são restaurados após a reinicialização

### PROBLEMAS CONHECIDOS

* [Bakers] Falha durante a cozedura com alguns drivers NVIDIA específicos
* [Exibição 3D] OpenGL: algumas cenas importadas podem não ser renderizadas
* [3D View] Pathtracer: desempenho lento ao atualizar texturas com mosaico/deslocamento ativado
* [Exibição 3D] Algumas propriedades do material de cores não são gerenciadas corretamente quando substituídas
* [Exibição 3D] As cenas com primitivas animadas não são suportadas corretamente
* [Exibição 3D] Ainda não há suporte para malha com vários UDims
* [Exibição 3D] Malha com vários UVs não é suportada no caso e pode resultar em renderização de material inválida
* [Exibição 3D] Não há suporte para Pathtracer em placas gráficas AMD
