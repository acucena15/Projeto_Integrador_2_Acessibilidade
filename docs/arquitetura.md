# 🏛️ RELATÓRIO DE ARQUITETURA E MODELAGEM
---

> **Projeto:** Sistema de Reserva de Salas Escolares  
> **Autor:** Açucena Alves Soares  
> **Status:** Em Revisão 🟡

---

## 📋 1. Visão Geral do Projeto

O sistema de **Reserva de Salas Escolares** visa resolver conflitos no agendamento manual de salas, auditórios e laboratórios em instituições de ensino. A solução oferece consultas em tempo real, validação automática de conflitos e fluxo de aprovação por perfil de usuário.

---

## 🔀 2. Diagrama de Fluxo de Processo (Mermaid)

```mermaid
graph TD
    A[Usuário realiza Login] --> B{Validar Perfil}
    B -->|Aluno / Professor| C[Consultar Calendário de Salas]
    C --> D[Selecionar Sala, Data e Horário]
    D --> E{Validação: Horário Disponível?}
    E -->|Não - Conflito| F[Exibir Mensagem: Sala Ocupada]
    E -->|Sim - Livre| G{Perfil do Solicitante?}
    G -->|Professor| H[Reserva Confirmada Automaticamente]
    G -->|Aluno| I[Solicitação Enviada para a Coordenação]
    I --> J{Aprovação da Coordenação?}
    J -->|Sim| H
    J -->|Não| K[Reserva Recusada com Justificativa]

erDiagram
    USUARIO ||--o{ RESERVA : solicita
    SALA ||--o{ RESERVA : possui
    
    USUARIO {
        int id_usuario PK
        string nome
        string email
        string perfil "Aluno / Professor / Coordenação"
    }
    
    SALA {
        int id_sala PK
        string nome_sala
        int capacidade
        string tipo_recurso "Laboratório / Auditório / Sala"
    }
    
    RESERVA {
        int id_reserva PK
        int id_usuario FK
        int id_sala FK
        date data_reserva
        time hora_inicio
        time hora_fim
        string status "Pendente / Aprovada / Recusada"
    }
