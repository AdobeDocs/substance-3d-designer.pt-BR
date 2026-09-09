---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-13-1.html"
breadcrumb-title: ''
description: Consulte as notas de versão do Substance 3D Designer versão 13.1 para saber mais sobre melhorias no gráfico de nós e suporte à exportação de AxF.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 13.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versão 13.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1289'
ht-degree: 1%

---


# Versão 13.1

O <b>Substance 3D Designer 13.1</b> adiciona muitas melhorias de qualidade de vida ao gráfico de nós, principalmente em relação a quadros, para aprimorar a experiência de criação de material. Há também a adição da exportação de AxF, que permite um fluxo de trabalho de interoperabilidade para usuários que trabalham com o formato AxF.

*Data de lançamento: 12 de dezembro de 2023*

![Banner do Substance 3D Designer 13.1](../../assets/24-library-hero-1920x620.png "banner do Substance 3D Designer 13.1")

## Melhorias para quadros

Os quadros são uma ferramenta obrigatória para mantê-lo um gráfico bem organizado e legível. Foi por isso que decidimos aperfeiçoá-los nesta nova versão.

### Expansão automática

À medida que o gráfico cresce, o conteúdo dos quadros pode precisar ser reorganizado. Os nós podem mudar para criar espaço para adições ou o conteúdo pode precisar ser espaçado mais para promover a legibilidade. Para facilitar esses ajustes, agora é possível expandir automaticamente um quadro ao mover os objetos incluídos: mantenha pressionado o <b>Shift</b> em qualquer ponto ao mover um objeto para que as bordas do quadro se ajustem automaticamente para manter esse objeto dentro de seus limites.

![expansão automática](../../assets/autoexpand.gif)

### Ajustar tamanho ao conteúdo

Conforme você faz ajustes no gráfico, um quadro pode não ser mais ajustado normalmente ao seu conteúdo. Esse novo comando permite ajustar automaticamente a posição e o tamanho do quadro para que ele se ajuste à extensão de seu conteúdo, com um preenchimento de uma célula de grade média. Se o quadro tiver uma descrição, ele será ajustado para usar qualquer espaço vazio ao lado da descrição, se possível.

![tamanho da imagem](../../assets/fitsize.gif)

### Descrições aprimoradas

Graças ao código HTML, agora é possível formatar o texto na descrição de um quadro. Isso também se aplica a comentários.

![richtext](../../assets/description-3.png)

### <b>...E muito mais!</b>

Muitas coisas foram repensadas, como regras de pertença para serem mais tolerantes, zonas de interação para redimensionar quadros facilmente, regras de ajuste para não desalinhar os nós na grade e o aspecto visual para trazer um pouco de frescor. Visite a [documentação](../../interface/the-graph-view/graph-items/frame/frame.md) dos quadros para saber mais.

## Melhorias na qualidade de vida

* <b>Melhorias no menu do nó: </b>para economizar tempo ao procurar o nó necessário, melhoramos um pouco o menu do nó. A busca agora é mais indulgente e lhe dará um resultado mesmo se não houver correspondência perfeita. Além disso, agora você pode usar a seta para cima para acessar diretamente o último elemento da lista.
* <b>Posicionamento do nó: </b>se você quiser ter um layout perfeito para o seu gráfico, essas duas pequenas alterações vão agradá-lo! Quando você copia/cola nós de um gráfico para outro, os nós colados agora são alinhados à grade principal. E quando você adiciona um nó em um link longo, este será colocado no meio da parte visível do link, para torná-lo visível em todas as situações.
* <b>Opções de exibição 2D: </b>se você for um usuário intensivo da [exibição 2D](../../interface/2d-view/2d-view.md), economizará tempo, pois opções como &#39;Mostrar tabuleiro de xadrez&#39;, &#39;Manter tamanho da exibição&#39;, &#39;Usar tamanho físico&#39; e &#39;Exibir divisão em blocos gráficos&#39; foram salvas, portanto, você não precisa defini-las novamente quando criar uma nova exibição 2D ou mesmo quando reiniciar o Designer.

## Exportação de AxF

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Ícone de arquivo AxF](../../assets/axf-file-icon.png "Ícone de arquivo AxF")

</td>
<td width="100.00%" style="border: 0;" valign="top">

AxF é um formato de [X-Rite](https://www.xrite.com/axf). Ele fornece uma maneira de capturar, armazenar, editar e comunicar características complexas de material usando dados numéricos em todo o fluxo de trabalho de design digital. Nas versões anteriores do Designer, você conseguia [importar arquivos AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) e depois melhorar a divisão em blocos gráficos ou adicionar efeitos de procedimento, mas depois tinha restrições para exportar alterações como um novo arquivo .sbsar.

Nesta nova versão, apresentamos a possibilidade de editar os materiais do AxF no local e, em seguida, [exportar suas alterações](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) como uma nova camada no arquivo AxF importado.

</td>
</tr>
</table>

![Exportar AxF](../../assets/exportaxf.gif)

## API

Finalmente, esta versão 13.1 continua a melhorar a API Python, adicionando mais duas possibilidades:

* <b> propriedades&#39;Visible if&#39;: </b>agora você pode definir essa propriedade para parâmetros, entradas e saídas de gráficos.
* <b>Ordem de gráficos Entradas/Saídas:</b> use sdsbscompgraph::reorderGraphInput e sdsbscompgraph::reorderGraphOutput para organizar os parâmetros conforme necessário.

>[!NOTE]
>
> O Designer 13.1 é a última versão principal baseada no Qt5, as próximas versões principais serão atualizadas para o Qt6. Isso pode ter um impacto em seus plug-ins personalizados.

## Notas de versão

### 13.1.0

*(Lançado em 12 de dezembro de 2023)*

### Adicionado

* [Frames] Expansão automática
* [Quadros] Alterar regras para definir quando um objeto pertence a um quadro
* [Quadros] Desabilitar escala de texto para descrição de quadros
* [Quadros] Ajustar tamanho ao conteúdo
* [Quadros] Novo padrão, passar o mouse e estados selecionados
* [Quadros] Ajustar à grade grande
* [Quadros] Descrição do código de HTML de suporte para Quadros
* [Quadros] Atualizar zonas de interação
* [Quadros] Atualizar aspecto visual
* [Gráfico] Criar o nó no meio do link visível em vez do meio do link
* [Gráfico] Exibe as propriedades de um item se ele for o único item com propriedades disponíveis em uma seleção
* [Gráfico] Remover a opção “Dimensionamento” para comentários no gráfico
* [Gráfico] Ajustar nós na grade principal ao copiar/colar
* [UX] Permitir pesquisa difusa no menu Nó e na pesquisa Biblioteca
* [UX] Criar loopN da lista de menus de Nó
* [AxF] Suporte para exportação de AxF
* [AxF] Desativar AxF no Linux
* [API] Defina a propriedade &#39;Visible if&#39; de parâmetros de gráficos, entradas e saídas usando a API Python
* [API] Definir a ordem de E/S do gráfico usando a API Python
* [Dependências] Atualizar aumento para 1.80.0
* [Dependências] Atualizar OpenSubdiv para 3.5.x
* [Dependências] Atualize o SDK FBX para 2020.3
* [Dependências] Atualizar NGL para 1.35.0.20
* [Gerenciamento de cores] Adicionar suporte para telas OCIO ICC
* [Níveis] Adicionar uma maneira de redefinir o histograma
* [Python] Avisar os usuários se o QtForPython não puder ser importado
* [Visualização 2D] Salvar o estado das opções de exibição
* [Visualização 3D] Adicionar a técnica de posição ao sombreador de informações de malha
* [Exportar] Adicione um botão “Salvar configurações” para salvar alterações nas opções de exportação

### Correções

* [Visualização 3D] Não é possível atribuir uma textura a uma entrada do tipo textura\_2d de um material MDL
* [AxF] Os identificadores de gráfico na lista de modelos podem ficar em branco
* [AxF] O campo do modelo de gráfico de Substance está em branco por padrão
* atlas scatter [Content]: comportamento incorreto em casos específicos
* [Content] Mapeador de Flood Fill: saída em branco quando todas as formas têm o mesmo tamanho de caixa
* [Content] FloodFill to Position: artefatos de imprecisão em algumas situações
* [Content] Saída de &#39;Specular&#39; incorreta no nó &#39;BaseColor/Metallic/Roughness converter&#39;
* [Conteúdo] A Máscara para o caminho não funciona na vertical não quadrada
* [Content] Descrição ausente para os nós Valor de entrada, Tons de cinza de entrada, Cor de entrada e Saída
* [Content] Descrição ausente para os nós Definir e Sequência
* [Content] Shape Splatter: artefatos de imprecisão na saída &#39;Splatter data 2&#39;
* [Engine] Booleanos em Processadores de valor sempre são avaliados como &#39;False&#39; (somente Apple Silicon)
* [Explorer] A ordem dos botões da barra de ferramentas é inconsistente entre o sistema operacional
* [Quadros] Não agarra nós ao mover uma quadro com o modificador CTRL
* [Mapa de gradiente] a opção redefinir tudo também deve redefinir o widget de gradiente
* [GraphRender] Alguns nós são renderizados em preto ao ajustar no modo de visualização
* [Graph] A visualização “Valor de entrada” fica presa a “Falso” ao ajustar o valor booleano padrão (somente Apple Silicon)
* [Gráfico] Os nós de ponto próximos à borda do Quadro não são movidos pelo Quadro
* [Interoperabilidade] O ícone de reenvio não é atualizado após o envio para a Substance 3D Stager
* [MDL] Impossível alterar a Aspereza em nós onde este parâmetro está disponível
* [MDL] Conexões inválidas no modelo &#39;AxF para Aspereza metálica&#39;
* [UI] A janela “Exportar saídas” pode ser minimizada (somente Windows)
* [UI] As imagens aparecem pixeladas na tela Sobre ao usar o dimensionamento de exibição
* [UI] Ferramentas de alinhamento de nós na barra de ferramentas de gráfico criam várias etapas de desfazer

### PROBLEMAS CONHECIDOS

* [AxF OpenGL Shader] Ala incorreta para distribuição anisotrópica
* [AxF OpenGL Shader] Aspereza padrão incorreta
* [AxF OpenGL Shader] Rotação incorreta da base do sombreamento
* [AxF OpenGL Shader] Detecção incorreta de raio abaixo do hemisfério
* [AxF OpenGL Shader] Detecção de contribuição incorreta
* [AxF] Os valores do mapa “Cor do Specular” estão incorretos quando exportados
* [AxF] A visualização e as texturas não são exibidas corretamente na caixa de diálogo “Importar AxF”
* [AxF] A propriedade “cc no refraction” não é injetada corretamente no modelo AxF para AxF
