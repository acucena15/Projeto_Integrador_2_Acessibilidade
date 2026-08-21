# 📚 Documento de Requisitos do Sistema CTBJ Conecta

## 📌 1. Requisitos Funcionais (RF)
*Representam as funcionalidades que o sistema deve ter:*

* **[RF01] Autenticação e Perfil:** O sistema deve permitir o login diferenciado para Alunos, Professores, Administradores (Coordenação) e Responsáveis por Setor.
* **[RF02] Consulta de Disponibilidade por Categoria:** O sistema deve exibir um calendário em tempo real categorizado com os status 🟢 Disponível, 🟡 Reservado e 🔴 Indisponível para Espaços, Informática, Agropecuária e Enfermagem.
* **[RF03] Solicitação de Reserva e Equipamentos:** O sistema deve permitir que o usuário selecione o local ou item específico (como o número do PC ou ferramenta), data, horário e justificativa de uso.
* **[RF04] Autorização do Professor e Moderação:** O sistema deve permitir que o professor valide solicitações de alunos e que a coordenação/responsável gerencie autorizações de espaços e chaves.
* **[RF05] Ficha Digital de Uso:** O sistema deve registrar os dados de utilização contendo aluno responsável, demais alunos presentes, horários reais de entrada/saída e confirmação de retirada e devolução de chaves ou equipamentos.
* **[RF06] Cancelamento:** O sistema deve permitir o cancelamento de uma reserva com antecedência.

## 🔒 2. Requisitos Não Funcionais (RNF)
*Representam os critérios técnicos e de qualidade do sistema:*

* **[RNF01] Regra de Concorrência:** O sistema **não** deve permitir dois agendamentos confirmados para a mesma sala, equipamento ou ferramenta no mesmo horário (prevenção de conflitos).
* **[RNF02] Multiplataforma e Usabilidade:** A interface deve ser simples, responsiva e funcionar nativamente no navegador (Web) e como aplicativo mobile, garantindo acesso mesmo em momentos de queda do SIGAA UFPI.
* **[RNF03] Desempenho:** A consulta ao catálogo de disponibilidade e status dos recursos deve carregar em menos de 2 segundos.
* **[RNF04] Segurança e Rastreabilidade:** As senhas dos usuários devem ser criptografadas e a Ficha Digital deve manter um histórico auditável de quem utilizou e retirou cada recurso.
