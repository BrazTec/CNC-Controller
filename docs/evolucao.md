# Evolução do Mini CNC Controller

## Montagem física

1. Levantamento de materiais e reaproveitamento dos conjuntos lineares dos mecanismos de DVD/disquete.
2. Preparação e alinhamento das bases de madeira, eixos e cama de impressão.
3. Construção do suporte de caneta e ajustes de deslocamento físico.
4. Instalação do Arduino Uno com CNC Shield V3 encaixada diretamente, drivers A4988 e alimentação externa.
5. Testes de movimento, calibração sem caneta, execução supervisionada e desenhos finalizados.

## Software: marcos registrados

| Versão / marco | Evolução |
| :-- | :-- |
| 0.8.24.x | Edição de G-code e confirmação de alterações |
| 8.29.1 | Prova de conceito local com LR-ASPP, DeepLabV3 e IS-Net |
| 8.29.2 | Interface de máscaras e confirmação manual |
| 8.29.3 | Composição e edição de regiões com histórico |
| 8.29.4 | Ajustes independentes por camada / tipo de traço |
| 8.29.5 | Ajustes de inferência local no Windows |
| 8.29.6 / 8.29.6.1 | Reorganização da interface e correções de usabilidade |
| **0.8.29.7** | Ajustes finais de interface e diagnósticos de imagem |

O histórico detalhado da implementação e seus arquivos permanecem **privados**, fora da publicação no GitHub. O desenvolvedor confirmou a operação da v0.8.29.7 no equipamento real; o relato não homologa automaticamente versões posteriores.

## Evolução posterior dos fontes locais

| Versão | Ampliação registrada |
| --- | --- |
| 0.8.29.8 | Enquadramento poligonal, confirmações de tratamento, inferência limitada à seleção com cancelamento e opção de cinzas fotográficos |
| 0.8.29.9 | Central Windows de validação/compilação e reorganização da documentação |

Essas versões não substituem a referência das capturas e do PDF. Os fontes e executáveis continuam privados. Veja o [estado da validação](validacao.md).
