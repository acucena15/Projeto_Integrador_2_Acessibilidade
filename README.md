# 🏫 CTBJ Conecta - Sistema de Agendamento, Reservas e Recursos

## 📌 Apresentação do Projeto
Este projeto consiste em uma plataforma (aplicativo e site) para automação e gestão do agendamento de salas de aula, laboratórios, auditórios, equipamentos e ferramentas no Colégio Técnico de Bom Jesus (CTBJ). Como uma alternativa leve e independente ao SIGAA UFPI, a solução elimina conflitos de horários, reduz a burocracia em papéis e otimiza o uso dos espaços e materiais por alunos e professores.

## 💡 Proposta de Valor
Proporcionar praticidade, transparência e rapidez na reserva de recursos escolares em tempo real. O sistema atende de forma personalizada os cursos de **Informática, Agropecuária e Enfermagem**, garantindo controle estrito de uso por meio de autorização prévia dos professores e preenchimento de uma Ficha Digital de uso e retirada de chaves/ferramentas.

# 👤 Personas do Sistema

### **Persona 1 (Professor): Prof. Carlos**
* **Perfil:** Docente dos cursos técnicos do CTBJ.
* **Necessidade:** Autorizar solicitações de alunos, realizar agendamentos diretos e instantâneos para suas aulas práticas (no campo da Agropecuária ou nos Laboratórios de TI) e acompanhar a Ficha Digital gerada para as suas turmas.

---

### **Persona 2 (Aluno): Maria**
* **Perfil:** Estudante do CTBJ (Enfermagem / Informática / Agropecuária).
* **Necessidade:** Solicitar o empréstimo de equipamentos, salas ou materiais técnicos, cadastrar os membros do seu grupo de trabalho e obter o QR Code/Comprovante Digital para retirar a chave do laboratório ou o kit de aulas.

---

### **Persona 3 (Funcionário / Técnico): Seu João**
* **Perfil:** Responsável pelo almoxarifado, chaveiro e manutenção dos setores.
* **Necessidade:** Acessar um painel simples para bipar/validar o QR Code do aluno, registrar a entrega/devolução de chaves e ferramentas, e alterar o status do recurso para 🔴 **Indisponível** quando precisar de manutenção.

---

### **Persona 4 (Diretor / Administrador): Diretora Ana**
* **Perfil:** Gestão e Direção do Colégio Técnico.
* **Necessidade:** Acessar o painel master antes do início do período letivo para cadastrar e validar as contas de Professores e Funcionários, garantindo a governança, a segurança e a hierarquia de acesso ao sistema.


## 💼 Modelo de Negócios: B2B / B2G
* **Modelo Escolhido:** B2B / B2G (Business to Business / Business to Government).
* **Justificativa:** O software é fornecido como solução *SaaS* (Software como Serviço) para a gestão da instituição (CTBJ/UFPI). Para os alunos, professores e coordenadores (usuários finais), o uso é 100% gratuito e integrado à rotina acadêmica via site e aplicativo mobile.
