# Calibração e execução supervisionada

O software permite configurar origem de trabalho, curso mecânico e contato da caneta. Há suporte a perfis de calibração, incluindo compensação Z por malha 3×3 e modo de mesa plana sem perfil.

## Fluxo utilizado na operação

1. Conferir fixação da caneta, isolamento, cabos, alimentação e espaço de movimento.
2. Conectar via USB/serial ao Arduino e confirmar o estado do GRBL 0.9j.
3. Verificar o sistema de coordenadas, a origem de trabalho e os limites mecânicos.
4. Preparar a calibração de Z de acordo com a montagem atual.
5. Ajustar o desenho e revisar dimensões, G-code, trajetória e parâmetros.
6. Validar por prévia e simulação offline antes de autorizar movimento físico.
7. Acompanhar todo o desenho e manter meios acessíveis de interrupção e desligamento.

**Segurança:** não reproduzir as medições do protótipo como valores genéricos de corrente de driver; inspecionar o sentido e encaixe das placas e drivers antes de energizar. Não conectar ou remover motores enquanto os drivers estiverem alimentados.

Nenhum perfil real de calibração ou configuração privada está disponibilizado neste repositório.
