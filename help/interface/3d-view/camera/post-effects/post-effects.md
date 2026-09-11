---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/camera/post-effects.html"
breadcrumb-title: ''
description: Aplique efeitos de pós-processamento à câmera de exibição 3D para aprimorar a visualização e a visualização do material.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Camera > Post effects
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pós-efeitos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 45cd3aec3baf2c35bae9e48540f6e7fb3a665541
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 4%

---


# Pós-efeitos

![Pós-efeitos](post-effects.resources/postEffects.png "Pós-efeitos"){zoomable="yes"}

Nas propriedades da câmera, você pode ativar os pós-efeitos para aprimorar as renderizações ou verificar as propriedades específicas do material.

Esses efeitos são desenvolvidos internamente e estão disponíveis somente para o Rasterizador e os [renderizadores](../../../../interface/3d-view/3d-renderers/3d-renderers.md) de GPU Pathtracer.

Qualquer pós-efeito habilitado no momento de salvar [recursos de cena 3D](../../../../resources/3d-scene-resource/3d-scene-resource.md) ou [arquivos de estado de cena](../../../../working-with-3d-scenes/working-with-3d-scenes.md) será salvo como parte do estado de cena.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Mapeamento de tons

</td>
<td style="border: 0;" valign="top">

### Florescer

</td>
<td style="border: 0;" valign="top">

### Profundidade de campo

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Mapeamento de tons

Remapeia as cores de renderização de acordo com algoritmos específicos e/ou tabelas de pesquisa (LUT).

Isso permite melhorar a consistência de cores entre aplicativos. Por exemplo, o mapeador de tons AgX também está disponível no Blender.

+++Reinhard


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXReinhard.jpg" alt="PostFXReinhard">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXReinhard](post-effects.resources/PostFXReinhard.jpg "PostFXReinhard")

+++

+++Atan


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXAtan.jpg" alt="PostFXAtan">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAtan](post-effects.resources/PostFXAtan.jpg "PostFXAtan")

+++

+++Exp


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXExp.jpg" alt="PostFXExp">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXExp](post-effects.resources/PostFXExp.jpg "PostFXExp")

+++

+++Log


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXLog.jpg" alt="PostFXLog">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXLog](post-effects.resources/PostFXLog.jpg "PostFXLog")

+++

+++Aces


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXAces.jpg" alt="PostFXAces">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAces](post-effects.resources/PostFXAces.jpg "PostFXAces")

+++

+++Hejl


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXHejl.jpg" alt="PostFXHejl">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXHejl](post-effects.resources/PostFXHejl.jpg "PostFXHejl")

+++

+++Neutro


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXNeutral.jpg" alt="PostFXNeutral">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXNeutral](post-effects.resources/PostFXNeutral.jpg "PostFXNeutral")

+++

+++Agx


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXAgx.jpg" alt="PostFXAgx">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAgx](post-effects.resources/PostFXAgx.jpg "PostFXAgx")

+++

+++Pbr neutro


<table>
  <tr>
    <td>
      <img src="post-effects.resources/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/PostFXPbrNeutral.jpg" alt="PostFXPbrNeutro">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](post-effects.resources/PostFXDisabled.jpg "PostFXDisabled")

![PostFXPbrNeutral](post-effects.resources/PostFXPbrNeutral.jpg "PostFXPbrNeutral")

+++

## Florescer

Simula o efeito na câmera de bordas de luzes sangrando para fora de áreas muito claras em áreas que recebem menos luz.

O efeito é influenciado pela iluminação, exposição da câmera e materiais de emissivo da cena.

+++Limiar
O valor de luminância acima do qual a flor deve ser visível.

*Esquerda: 1.0 / Direita: 4.0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/bloomThreshold1.jpg" alt="bloomThreshold1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/bloomThreshold4.jpg" alt="bloomThreshold4">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![bloomThreshold1](post-effects.resources/bloomThreshold1.jpg "bloomThreshold1")

![bloomThreshold4](post-effects.resources/bloomThreshold4.jpg "bloomThreshold4")

+++

+++Queda
O gradiente de atenuação da flor, em que um valor mais baixo resulta em um raio de flor mais curto.

*Esquerda: 1.0 / Direita: 0.6*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/bloomFalloff1.jpg" alt="bloomFalloff1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/bloomFalloff0-6.jpg" alt="bloomFalloff0-6">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![bloomFalloff1](post-effects.resources/bloomFalloff1.jpg "bloomFalloff1")

![bloomFalloff0-6](post-effects.resources/bloomFalloff0-6.jpg "bloomFalloff0-6")

+++

+++Nível
A intensidade da flor. Um valor mais alto resulta em bordas mais claras e mais brilhantes.

*Esquerda: 8.0 / Direita: 2.0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/bloomLevel8.jpg" alt="bloomLevel8">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/bloomLevel2.jpg" alt="bloomLevel2">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![bloomLevel8](post-effects.resources/bloomLevel8.jpg "bloomLevel8")

![nívelFlor2](post-effects.resources/bloomLevel2.jpg "nívelFlor2")

+++

+++Mudança de cor
Desloca o matiz das áreas afetadas pela flor para cores mais quentes.

*Esquerda: 0.0 / Direita: 0.8*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/bloomColorShift0.jpg" alt="bloomColorShift0">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/bloomColorShift0-8.jpg" alt="bloomColorShift0-8">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![bloomColorShift0](post-effects.resources/bloomColorShift0.jpg "bloomColorShift0")

![bloomColorShift0-8](post-effects.resources/bloomColorShift0-8.jpg "bloomColorShift0-8")

+++

## Profundidade de campo

Simula o fenômeno óptico causado pelas lentes da câmera, em que os objetos mais próximos e distantes da distância de foco ficam desfocados.

O efeito é afetado pelos parâmetros “F-Stop” e “Distância de foco” da câmera.

>[!TIP]
>
> Para ajustar rapidamente o foco da câmera, coloque o cursor no local de uma cena que deseja em foco e pressione Ctrl+LMB (Windows) ou Cmd+LMB (macOS) para definir automaticamente a distância de foco para esse local.

+++Raio máximo
O raio máximo do efeito de desfoque.

*Esquerda: 32.0 / Direita: 4.0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/depthOfFieldMaxRadius32.jpg" alt="depthOfFieldMaxRadius32">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/depthOfFieldMaxRadius4.jpg" alt="depthOfFieldMaxRadius4">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![depthOfFieldMaxRadius32](post-effects.resources/depthOfFieldMaxRadius32.jpg "depthOfFieldMaxRadius32")

![depthOfFieldMaxRadius4](post-effects.resources/depthOfFieldMaxRadius4.jpg "depthOfFieldMaxRadius4")

+++

+++Resistência composta
A magnitude do efeito de desfoque da distância de foco para fora.

*Esquerda: 0.2 / Direita: 0.05*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/depthOfFieldCompositeStrength0-2.jpg" alt="depthOfFieldCompositeStrength0-2">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/depthOfFieldCompositeStrength0-05.jpg" alt="depthOfFieldCompositeStrength0-05">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![depthOfFieldCompositeStrength0-2](post-effects.resources/depthOfFieldCompositeStrength0-2.jpg "depthOfFieldCompositeStrength0-2")

![depthOfFieldCompositeStrength0-05](post-effects.resources/depthOfFieldCompositeStrength0-05.jpg "depthOfFieldCompositeStrength0-05")

+++

+++Desvio longitudinal
A intensidade do desvio que ocorre fora da distância do foco.

O Desvio simula como diferentes comprimentos de onda de luz têm distâncias focais ligeiramente diferentes, resultando em cores que parecem estar deslocadas e com diferenças sutis de foco.

*Esquerda: 0.0 / Direita: 1.0*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/depthOfFieldLongitudinalAberration0.jpg" alt="depthOfFieldLongitudinalAberration0">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/depthOfFieldLongitudinalAberration1.jpg" alt="depthOfFieldLongitudinalAberration1">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![depthOfFieldLongitudinalAberration0](post-effects.resources/depthOfFieldLongitudinalAberration0.jpg "depthOfFieldLongitudinalAberration0")

![depthOfFieldLongitudinalAberration1](post-effects.resources/depthOfFieldLongitudinalAberration1.jpg "depthOfFieldLongitudinalAberration1")

+++

+++Desvio acromático
Especifica se o desvio deve ser acromático, o que significa que algumas ou todas as cores têm a mesma distância focal.

Isso faz com que o efeito de desfoque pareça estar mais uniformemente distribuído.

*Esquerda: Verdadeiro / Direita: Falso*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/depthOfFieldAchromaticAberrationYes.jpg" alt="depthOfFieldAchromaticAberrationYes">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/depthOfFieldAchromaticAberrationNo.jpg" alt="depthOfFieldAchromaticAberrationNo">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticAberrationYes](post-effects.resources/depthOfFieldAchromaticAberrationYes.jpg "depthOfFieldAchromaticAberrationYes")

![depthOfFieldAchromaticAberrationNo](post-effects.resources/depthOfFieldAchromaticAberrationNo.jpg "depthOfFieldAchromaticAberrationNo")

+++

+++Olho de gato
Ativa o efeito de olho do gato na cena, que simula como a luz que entra em um ângulo oblíquo não entra em um disco, mas em um oval irregular, causando distorção.

Esse efeito é mais pronunciado em aberturas mais altas, ou seja, valores de parada F mais baixos.

*Esquerda: Verdadeiro / Direita: Falso*



<table>
  <tr>
    <td>
      <img src="post-effects.resources/depthOfFieldAchromaticCatsEyeYes.jpg" alt="depthOfFieldAchromaticCatsEyeYes">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="post-effects.resources/depthOfFieldAchromaticCatsEyeNo.jpg" alt="depthOfFieldAchromaticCatsEyeNo">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticCatsEyeYes](post-effects.resources/depthOfFieldAchromaticCatsEyeYes.jpg "depthOfFieldAchromaticCatsEyeYes")

![depthOfFieldAchromaticCatsEyeNo](post-effects.resources/depthOfFieldAchromaticCatsEyeNo.jpg "depthOfFieldAchromaticCatsEyeNo")

+++
