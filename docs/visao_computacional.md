# Visão computacional e IA aplicada

O objetivo é transformar uma imagem em traços adequados a uma pequena área física. Essa transformação exige escolher o assunto, controlar detalhes e separar o que deve ser desenhado. A IA atua como assistência de segmentação dentro desse fluxo.

## Processamento clássico e inferência aprendida

| Etapa | Abordagem | Papel do operador |
| --- | --- | --- |
| Importação e enquadramento | Orientação, região de interesse e geometria da seleção | Definir assunto e área útil |
| Pré-processamento | Nitidez, contraste local e redução de ruído | Comparar prévia e confirmar os ajustes |
| Proposta de máscara | Inferência local de modelo pré-treinado | Escolher alternativa e revisar o resultado |
| Edição e composição | Regiões conectadas, pincel, união, subtração e interseção | Corrigir a seleção antes de aplicar |
| Extração de camadas | Contornos, detalhes, texturas e sombras | Ajustar densidade, sensibilidade e escala |
| Trajetórias e G-code | Planejamento, ordenação, orientação e validação | Conferir prévia e preparar a execução |

A máscara delimita regiões; não é o próprio percurso de desenho. A extração de traços continua sendo uma etapa distinta. Uma região conectada também não equivale necessariamente a uma instância semântica separada.

## Modelos avaliados

- **LR-ASPP:** alternativa de segmentação semântica disponível no TorchVision.
- **DeepLabV3:** outra alternativa de segmentação semântica do TorchVision.
- **IS-Net:** alternativa associada à segmentação dicotômica e separação de assunto/fundo.

O histórico de desenvolvimento registra uma PoC de 12 inferências em quatro imagens. Esse número descreve o experimento exploratório, não um benchmark representativo nem uma validação da precisão dos desenhos físicos. Não se publicam métricas de acurácia sem referência adequada, nem se converte área selecionada em índice de confiança.

A escolha depende da imagem: pelos, cabelo, ilustrações estilizadas e cenas com várias pessoas podem exigir modelos e correções diferentes. As redes e os pesos são de terceiros. A contribuição autoral está na avaliação, integração local, interface, edição de máscaras e aplicação das políticas às camadas, sem reivindicar criação ou treinamento das arquiteturas.

## Evolução do fluxo

O material histórico da v0.8.29.7 registra máscaras assistidas, composição e políticas por camada. Na evolução posterior dos fontes, a v0.8.29.8 acrescentou enquadramento poligonal com pontos intermediários, confirmação de tratamento, sugestões conservadoras de ajustes, análise limitada à seleção e cancelamento da inferência. Esses avanços não são apresentados como visíveis nas capturas antigas.

As sugestões de qualidade são heurísticas indicativas. Não recuperam informação ausente e não são uma nota universal de foco. A detecção de rosto auxilia a priorização do recorte; não é reconhecimento de identidade nem reconstrução facial.

## Limites e comprovação

Este portfólio não declara IA generativa de imagens, treinamento de rede própria ou geração autônoma de desenhos por um modelo. Os vídeos documentam o equipamento em operação, sem comprovar que cada desenho passou por todos os modelos de segmentação.

Um próximo registro útil é documentar, para uma imagem autorizada, a entrada, a máscara proposta, a correção humana, as camadas selecionadas e o desenho resultante na mesma escala. Isso permitiria relacionar a contribuição da segmentação ao resultado sem misturar versões ou inferir métricas inexistentes.

## Referências dos modelos

- [TorchVision e pesos pré-treinados](https://docs.pytorch.org/vision/stable/models.html)
- [LR-ASPP no TorchVision](https://docs.pytorch.org/vision/stable/models/lraspp.html)
- [DeepLabV3 no TorchVision](https://docs.pytorch.org/vision/stable/models/deeplabv3.html)
- [Projeto DIS e IS-Net](https://github.com/xuebinqin/DIS)

Código, pesos, modelos exportados e imagens privadas não são distribuídos neste portfólio.
