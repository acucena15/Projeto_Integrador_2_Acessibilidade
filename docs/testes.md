# Relatório de Validação e Testes — CTBJ Conecta

Este documento apresenta os cenários de testes funcionais, evidências de uso de Inteligência Artificial e a validação do sistema **CTBJ Conecta**.

---

## 1. Cenários de Testes Funcionais

| ID | Funcionalidade Testada | Entrada / Ação | Resultado Esperado | Status |
| :--- | :--- | :--- | :--- | :---: |
| **TC01** | Permissão de Aluno | Aluno tenta reservar espaço | Mensagem de bloqueio por regra RBAC | Passou ✅ |
| **TC02** | Permissão de Professor | Professor envia solicitação | Status alterado para "Pendente" | Passou ✅ |
| **TC03** | Validação de Conflito | Agendamento no mesmo horário | Sistema impede reserva duplicada | Passou ✅ |
| **TC04** | Aprovação de Reserva | Coordenador aprova o pedido | Status alterado para "Confirmado" | Passou ✅ |

---

## 2. Evidências de Validação e Uso de I.A.

* **Apoio no Protótipo / Telas:** Auxílio de Inteligência Artificial para estruturar componentes visuais e layout.
* **Demonstração Prática:** A validação do fluxo foi registrada em formato de vídeo de aplicação experimental do usuário.

---

## 3. Conclusão
O sistema atendeu a todas as regras de negócio propostas, mantendo a solução leve, segura e totalmente alinhada ao escopo do Projeto Integrador II.
