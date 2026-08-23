# 📌 Documento de Requisitos — CTBJ Conecta

## 1. Requisitos Funcionais (RF)

* **[RF01] Gestão de Acessos pelo Diretor (Admin):** O sistema deve permitir que o Diretor/Administrador cadastre e gerencie previamente as contas de Professores e Funcionários/Técnicos antes do uso institucional.
* **[RF02] Autocadastro de Alunos com Validação:** O sistema deve permitir que os alunos criem suas próprias contas informando matrícula, e-mail institucional e curso (Informática, Agropecuária ou Enfermagem).
* **[RF03] Autenticação e Perfis (RBAC):** O sistema deve oferecer login e visões diferenciadas para Alunos, Professores, Funcionários/Técnicos e Direção/Coordenação.
* **[RF04] Consulta por Categoria e Status em Tempo Real:** O sistema deve exibir a infraestrutura dividida em 4 categorias (📍 Espaços, 🖥️ Informática, 🌱 Agropecuária e 🩺 Enfermagem) com os indicadores visuais 🟢 **Disponível**, 🟡 **Reservado** e 🔴 **Indisponível**.
* **[RF05] Solicitação com Agrupamento e Item Específico:** O sistema deve permitir que o aluno selecione o item/sala específico (número do PC, chave do laboratório ou ferramenta), informe data, horário, justificativa, indique o Professor Autorizador e cadastre os demais alunos do grupo.
* **[RF06] Autorização e Reserva Direta do Professor:** O sistema deve permitir que o professor aprove ou recuse solicitações de alunos em um clique, além de realizar reservas diretas com aprovação automática para suas próprias aulas.
* **[RF07] Painel do Funcionário (Entrega e Devolução):** O sistema deve disponibilizar uma interface para o funcionário/técnico validar a retirada e devolução de chaves e equipamentos via QR Code, registrando o estado do bem.
* **[RF08] Ficha e Comprovante Digital:** O sistema deve gerar um comprovante digital automático com código único de validação (`CTBJ-XXXXX`) e QR Code contendo aluno responsável, integrantes do grupo, professor autorizador e horários.
* **[RF09] Histórico e Cancelamento:** O sistema deve permitir o cancelamento de agendamentos dentro do prazo estipulado e manter um histórico auditável de utilizações.

---

## 🔒 2. Requisitos Não Funcionais (RNF)

* **[RNF01] Prevenção de Conflitos (Regra de Concorrência):** O sistema não deve permitir agendamentos duplicados ou sobrepostos para o mesmo recurso, ferramenta ou chave no mesmo intervalo de horário.
* **[RNF02] Usabilidade e Layout Responsivo:** A interface deve ser responsiva e adaptada para dispositivos móveis e desktops, utilizando a identidade e paleta institucional do CTBJ (Azul Marinho `#212868` e Azul Cyan `#00AEEF`).
* **[RNF03] Desempenho e Carregamento:** A consulta ao catálogo de categorias e aos status dos recursos deve responder em menos de 2 segundos.
* **[RNF04] Segurança e Rastreabilidade:** As senhas devem ser criptografadas no banco de dados e as Fichas Digitais devem registrar de forma inalterável o histórico de entradas, saídas e responsáveis pela infraestrutura.
* **[RNF05] Disponibilidade Multiplataforma:** O sistema deve funcionar via navegador Web como aplicação independente para garantir o fluxo de reservas mesmo em momentos de instabilidade nos sistemas tradicionais.
* 
