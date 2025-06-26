
Escopo geral da satividades

| **Tarefa** | **Detalhamento Técnico** |
|-----------|---------------------------|
| Alterar o software Cronos para controle de lote e serialização | Implementar estrutura de dados que permita registrar e rastrear lote e número de série por item; ajustar telas e banco de dados. |
| Integrar consulta ao SAP com base em item + lote | Consumir API ou serviço (ex: Service Layer, DI Server) para validar informações de estoque por item/lote diretamente no SAP. |
| Adaptar o Cronos para operação com redundância local | Implementar persistência local temporária dos dados em caso de perda de conexão com a rede. |
| Criar banco de dados local por máquina | Banco leve (SQLite, LiteDB) com estrutura replicável para operação offline e reenvio posterior. |
| Criar banco de dados em nuvem (Azure) | Estrutura centralizada para consolidação dos apontamentos. Implementar política de segurança e replicação. |
| Implementar fallback de rede com sincronização posterior | Detecção automática de falha de conexão e reprocessamento dos apontamentos após retorno da rede. |
| Atualizar firmware dos coletores unidimensionais | Garantir compatibilidade com novo padrão de etiqueta (importada), ajustar leitura e formatação do dado capturado. |
| Configurar coletores para leitura dos códigos utilizados | Definir padrão (EAN, Code128, QR), ajustar prefixos/sufixos e comportamento de leitura. |
| Configurar firmware da impressora Zebra | Ajustar linguagem ZPL, calibragem de sensores e modo de impressão contínuo/discreto conforme layout exigido. |
| Desenvolver gerador de etiquetas ZPL dinâmico | Script parametrizado com variáveis para lote, produto, validade, SN, operador e conformidade. |
| Ajustar DPI e área de impressão | Definir resolução (203 ou 300 DPI), dimensões da etiqueta e margens para leitura sem falhas. |
| Instalar software nas máquinas operacionais | Garantir pré-requisitos (permissões, drivers, rede), realizar instalação controlada com validação pós-instalação. |
| Realizar testes de leitura e apontamento | Testes com código real, verificação de consistência entre etiquetas, SAP e banco local. |
| Testar operação offline (failover por máquina) | Simular perda de rede, capturar apontamentos, validar reprocessamento automático ao restabelecer conexão. |
| Validar integração SAP x Cronos x etiquetas físicas | Conferência cruzada de informações entre sistemas e leitura de etiquetas. |
| Documentar a solução final | Criar manual técnico com instruções de operação, fallback, manutenção e pontos de integração. |

Developed by eonferraz
