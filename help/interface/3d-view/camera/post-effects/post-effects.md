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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 4%

---


# Pós-efeitos

![Pós-efeitos](../../../../assets/postEffects.png "Pós-efeitos"){zoomable="yes"}

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
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXReinhard.jpg" alt="PostFXReinhard">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXReinhard](../../../../assets/PostFXReinhard.jpg "PostFXReinhard")

+++

+++Atan


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAtan.jpg" alt="PostFXAtan">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAtan](../../../../assets/PostFXAtan.jpg "PostFXAtan")

+++

+++Exp


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXExp.jpg" alt="PostFXExp">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXExp](../../../../assets/PostFXExp.jpg "PostFXExp")

+++

+++Log


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXLog.jpg" alt="PostFXLog">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXLog](../../../../assets/PostFXLog.jpg "PostFXLog")

+++

+++Aces


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAces.jpg" alt="PostFXAces">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAces](../../../../assets/PostFXAces.jpg "PostFXAces")

+++

+++Hejl


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXHejl.jpg" alt="PostFXHejl">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXHejl](../../../../assets/PostFXHejl.jpg "PostFXHejl")

+++

+++Neutro


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXNeutral.jpg" alt="PostFXNeutral">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXNeutral](../../../../assets/PostFXNeutral.jpg "PostFXNeutral")

+++

+++Agx


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAgx.jpg" alt="PostFXAgx">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAgx](../../../../assets/PostFXAgx.jpg "PostFXAgx")

+++

+++Pbr neutro


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXPbrNeutral.jpg" alt="PostFXPbrNeutro">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXPbrNeutral](../../../../assets/PostFXPbrNeutral.jpg "PostFXPbrNeutral")

+++

## Florescer

Simula o efeito na câmera de bordas de luzes sangrando para fora de áreas muito claras em áreas que recebem menos luz.

O efeito é influenciado pela iluminação, exposição da câmera e materiais emissivos da cena.

+++Limiar
O valor de luminância acima do qual a flor deve ser visível.

*Esquerda: 1.0 / Direita: 4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomThreshold1.jpg" alt="bloomThreshold1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/bloomThreshold4.jpg" alt="bloomThreshold4">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![bloomThreshold1](../../../../assets/bloomThreshold1.jpg "bloomThreshold1")

![bloomThreshold4](../../../../assets/bloomThreshold4.jpg "bloomThreshold4")

+++

+++Queda
O gradiente de atenuação da flor, em que um valor mais baixo resulta em um raio de flor mais curto.

*Esquerda: 1.0 / Direita: 0.6*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomFalloff1.jpg" alt="bloomFalloff1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/bloomFalloff0-6.jpg" alt="bloomFalloff0-6">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![bloomFalloff1](../../../../assets/bloomFalloff1.jpg "bloomFalloff1")

![bloomFalloff0-6](../../../../assets/bloomFalloff0-6.jpg "bloomFalloff0-6")

+++

+++Nível
A intensidade da flor. Um valor mais alto resulta em bordas mais claras e mais brilhantes.

*Esquerda: 8.0 / Direita: 2.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomLevel8.jpg" alt="bloomLevel8">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/bloomLevel2.jpg" alt="bloomLevel2">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![bloomLevel8](../../../../assets/bloomLevel8.jpg "bloomLevel8")

![nívelFlor2](../../../../assets/bloomLevel2.jpg "nívelFlor2")

+++

+++Mudança de cor
Desloca o matiz das áreas afetadas pela flor para cores mais quentes.

*Esquerda: 0.0 / Direita: 0.8*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomColorShift0.jpg" alt="bloomColorShift0">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/bloomColorShift0-8.jpg" alt="bloomColorShift0-8">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![bloomColorShift0](../../../../assets/bloomColorShift0.jpg "bloomColorShift0")

![bloomColorShift0-8](../../../../assets/bloomColorShift0-8.jpg "bloomColorShift0-8")

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
      <img src="../../../../assets/depthOfFieldMaxRadius32.jpg" alt="depthOfFieldMaxRadius32">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius4.jpg" alt="depthOfFieldMaxRadius4">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![depthOfFieldMaxRadius32](../../../../assets/depthOfFieldMaxRadius32.jpg "depthOfFieldMaxRadius32")

![depthOfFieldMaxRadius4](../../../../assets/depthOfFieldMaxRadius4.jpg "depthOfFieldMaxRadius4")

+++

+++Resistência composta
A magnitude do efeito de desfoque da distância de foco para fora.

*Esquerda: 0.2 / Direita: 0.05*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-2.jpg" alt="depthOfFieldCompositeStrength0-2">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-05.jpg" alt="depthOfFieldCompositeStrength0-05">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![depthOfFieldCompositeStrength0-2](../../../../assets/depthOfFieldCompositeStrength0-2.jpg "depthOfFieldCompositeStrength0-2")

![depthOfFieldCompositeStrength0-05](../../../../assets/depthOfFieldCompositeStrength0-05.jpg "depthOfFieldCompositeStrength0-05")

+++

+++Desvio longitudinal
A intensidade do desvio que ocorre fora da distância do foco.

O Desvio simula como diferentes comprimentos de onda de luz têm distâncias focais ligeiramente diferentes, resultando em cores que parecem estar deslocadas e com diferenças sutis de foco.

*Esquerda: 0.0 / Direita: 1.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration0.jpg" alt="depthOfFieldLongitudinalAberration0">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration1.jpg" alt="depthOfFieldLongitudinalAberration1">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![depthOfFieldLongitudinalAberration0](../../../../assets/depthOfFieldLongitudinalAberration0.jpg "depthOfFieldLongitudinalAberration0")

![depthOfFieldLongitudinalAberration1](../../../../assets/depthOfFieldLongitudinalAberration1.jpg "depthOfFieldLongitudinalAberration1")

+++

+++Desvio acromático
Especifica se o desvio deve ser acromático, o que significa que algumas ou todas as cores têm a mesma distância focal.

Isso faz com que o efeito de desfoque pareça estar mais uniformemente distribuído.

*Esquerda: Verdadeiro / Direita: Falso*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationYes.jpg" alt="depthOfFieldAchromaticAberrationYes">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationNo.jpg" alt="depthOfFieldAchromaticAberrationNo">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticAberrationYes](../../../../assets/depthOfFieldAchromaticAberrationYes.jpg "depthOfFieldAchromaticAberrationYes")

![depthOfFieldAchromaticAberrationNo](../../../../assets/depthOfFieldAchromaticAberrationNo.jpg "depthOfFieldAchromaticAberrationNo")

+++

+++Olho de gato
Ativa o efeito de olho do gato na cena, que simula como a luz que entra em um ângulo oblíquo não entra em um disco, mas em um oval irregular, causando distorção.

Esse efeito é mais pronunciado em aberturas mais altas, ou seja, valores de parada F mais baixos.

*Esquerda: Verdadeiro / Direita: Falso*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg" alt="depthOfFieldAchromaticCatsEyeYes">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg" alt="depthOfFieldAchromaticCatsEyeNo">
      <br><i>Depois</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticCatsEyeYes](../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg "depthOfFieldAchromaticCatsEyeYes")

![depthOfFieldAchromaticCatsEyeNo](../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg "depthOfFieldAchromaticCatsEyeNo")

+++
