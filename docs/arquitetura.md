# 🏛️ RELATÓRIO DE ARQUITETURA E MODELAGEM - CTBJ CONECTA
---

> **Projeto:** CTBJ Conecta (Web & App Mobile)  
> **Autora:** Açucena Alves Soares  
> **Instituição:** Colégio Técnico de Bom Jesus (CTBJ - UFPI)

---

## 📋 1. Visão Geral do Sistema
O **CTBJ Conecta** é uma solução integradora desenvolvida para gerenciar a reserva, empréstimo e controle de utilização de **Espaços, Equipamentos e Ferramentas** dos cursos de Informática, Agropecuária e Enfermagem. O fluxo exige autorização do professor e preenchimento da **Ficha Digital de Uso**.

---

## 🔀 2. Diagrama de Fluxo de Processo (Mermaid)

```mermaid
graph TD
    A[Usuário abre o CTBJ Conecta Web/App] --> B{Possui Acesso / Perfil?}
    B -->|Não Autorizado| C[Acesso Negado]
    B -->|Aluno / Professor| D[Selecionar Categoria: Espaços, Informática, Agro ou Enfermagem]
    D --> E[Verificar Status: Livre 🟢 / Reservado 🟡 / Indisponível 🔴]
    E --> F[Solicitar Reserva / Empréstimo]
    F --> G{Exige Autorização do Professor?}
    G -->|Sim| H[Enviar Notificação para Validação do Professor]
    H --> I{Professor Aprovou?}
    I -->|Não| J[Reserva Recusada com Justificativa]
    I -->|Sim| K[Preencher Ficha Digital de Uso e Alunos Envolvidos]
    G -->|Não / Sou Professor| K
    K --> L[Retirar Chave / Equipamento com o Responsável]
    L --> M[Registrar Horário de Entrada e N° do PC/Ferramenta]
    M --> N[Uso do Recurso]
    N --> O[Registrar Horário de Saída e Devolução da Chave]
    O --> P[Status Concluído no Sistema 🟢]

erDiagram
    USUARIO ||--o{ SOLICITACAO : realiza
    USUARIO ||--o{ SOLICITACAO : autoriza_como_professor
    RECURSO ||--o{ SOLICITACAO : eh_reservado
    SOLICITACAO ||--|| FICHA_USO : gera

    USUARIO {
        int id_usuario PK
        string nome
        string matricula
        string curso
        string perfil
    }

    RECURSO {
        int id_recurso PK
        string nome_recurso
        string categoria
        string tipo
        string status
    }

    SOLICITACAO {
        int id_solicitacao PK
        int id_aluno FK
        int id_professor_autorizador FK
        int id_recurso FK
        date data
        time hora_inicio
        time hora_fim
        string status_aprovacao
    }

    FICHA_USO {
        int id_ficha PK
        int id_solicitacao FK
        string lista_alunos_presentes
        string identificador_pc_ou_ferramenta
        time hora_entrada_real
        time hora_saida_real
        boolean chave_retirada
        boolean chave_devolvida
    }
