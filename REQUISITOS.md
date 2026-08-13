# 📚 Documento de Requisitos do Sistema de Reserva de Salas

## 📌 1. Requisitos Funcionais (RF)
*Representam as funcionalidades que o sistema deve ter:*

* **[RF01] Autenticação e Perfil:** O sistema deve permitir o login diferenciado para Alunos, Professores e Administradores (Coordenação).
* **[RF02] Consulta de Disponibilidade:** O sistema deve exibir um calendário em tempo real com as salas, laboratórios, horários livres e ocupados.
* **[RF03] Solicitação de Reserva:** O sistema deve permitir que o usuário selecione uma sala, data, horário inicial/final e justificativa do uso.
* **[RF04] Aprovação de Agendamento:** O sistema deve permitir que a administração/coordenação aprove ou recuse solicitações de reserva feitas por alunos.
* **[RF05] Cancelamento:** O sistema deve permitir o cancelamento de uma reserva com antecedência.


## 🔒 2. Requisitos Não Funcionais (RNF)
*Representam os critérios técnicos e de qualidade do sistema:*

* **[RNF01] Regra de Concorrência:** O sistema **não** deve permitir dois agendamentos confirmados para a mesma sala no mesmo horário (prevenção de conflitos).
* **[RNF02] Usabilidade:** A interface deve ser simples e responsiva, funcionando bem tanto no navegador do computador quanto no celular.
* **[RNF03] Desempenho:** A consulta ao calendário de disponibilidade deve carregar em menos de 2 segundos.
* **[RNF04] Segurança:** As senhas dos usuários devem ser armazenadas de forma criptografada no banco de dados.
