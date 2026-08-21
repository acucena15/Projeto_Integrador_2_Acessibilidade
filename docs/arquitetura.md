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
    A[Inicio] --> B{Possui Acesso?}
    B -->|Nao| C[Acesso Negado]
    B -->|Sim| D[Selecionar Categoria]
    D --> E[Verificar Status]
    E --> F[Solicitar Reserva]
    F --> G{Exige Autorizacao?}
    G -->|Sim| H[Notificar Professor]
    H --> I{Aprovou?}
    I -->|Nao| J[Reserva Recusada]
    I -->|Sim| K[Preencher Ficha Digital]
    G -->|Nao| K
    K --> L[Retirar Chave]
    L --> M[Registrar Entrada]
    M --> N[Uso do Recurso]
    N --> O[Registrar Saida]
    O --> P[Status Concluido]
erDiagram
    USUARIO ||--o{ SOLICITACAO : realiza
    USUARIO ||--o{ SOLICITACAO : autoriza
    RECURSO ||--o{ SOLICITACAO : reservado
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
