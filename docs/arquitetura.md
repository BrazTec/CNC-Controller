# Arquitetura funcional

## Integração do sistema

```text
Imagem importada
       |
Processamento 2D / enquadramento
       |
Contornos, camadas, máscaras e assistência de visão
       |
Planejamento / otimização de trajetórias
       |
Geração e edição de G-code
       |
Prévia e simulação offline
       |
Calibração e confirmação supervisionada
       |
Comunicação USB/serial
       |
Arduino Uno -> GRBL 0.9j
       |
CNC Shield V3 -> A4988 -> Motores X/Y/Z
```

A **lógica da aplicação** permanece no computador. A **lógica de movimento** está no firmware GRBL instalado no Arduino. A **CNC Shield V3**, encaixada diretamente no Uno, disponibiliza os conectores para os drivers e a alimentação externa da etapa de motores.

## Componentes funcionais

| Camada | Papel |
| :-- | :-- |
| Interface gráfica | Importação, ajustes, prévias, edição, calibração e monitoramento |
| Processamento de imagem | Contornos, detalhes, sombras, máscaras, resolução e camadas |
| Planejamento de movimento | Trajetórias 2D, parâmetros de deslocamento e G-code |
| Simulação e validação | Conferência antes do acionamento físico |
| Comunicação serial | Consulta de estado e transmissão de comandos ao GRBL |
| Hardware | Arduino Uno, CNC Shield V3, A4988 e mecanismos XYZ |

A publicação descreve a arquitetura **em nível funcional**. **Não inclui o código-fonte do aplicativo nem uma árvore de diretórios de implementação.**

## Distinção entre processamento e IA

A segmentação por modelos pré-treinados propõe máscaras; a extração de camadas transforma a imagem em traços. A otimização organiza os percursos, e o firmware executa os comandos aceitos. Nenhuma dessas etapas equivale a uma medição mecânica independente. Consulte o [fluxo de visão computacional e IA](visao_computacional.md).
