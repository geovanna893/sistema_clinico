# Sistema Clínico — Clínica Long Life

Sistema web para gestão de agendamentos de consultas médicas, controle de pacientes e médicos em clínicas.

---

## 👥 Integrantes

- Geovanna Alves Rodrigues
- Luan Matos
- Lucas Kauan
- José Carlos
- Natanael Reis

## 🎯 Objetivo

Otimizar processos administrativos de clínicas médicas, reduzindo erros de agendamento e facilitando o controle de pacientes, médicos e consultas por meio de uma interface web intuitiva.

---

## ⚙️ Principais Funcionalidades

- **Autenticação** — login e logout com controle de acesso por sessão
- **Cadastro de pacientes** — com validação de CPF, nome completo, telefone e data de nascimento
- **Cadastro de médicos** — com validação de CRM, especialidade e horário de atendimento
- **Agendamento de consultas** — busca de paciente por CPF, seleção de médico e data/hora, com validações de:
  - Dias úteis (segunda a sexta)
  - Horários permitidos: 09:00–12:00 e 14:00–18:00
  - Conflito de horário por médico
- **Listagem de consultas** — com alteração de status (Agendada, Ocorrendo, Realizada) e exclusão
- **Calendário de consultas** — visualização via FullCalendar, com filtro por médico
- **Exclusão de pacientes e médicos**

---

## 🛠️ Tecnologias

- **Python 3** + **Django**
- **Bootstrap 5** 
- **jQuery** + **AJAX**
- **FullCalendar 6**
- **SQLite**
---

## 📁 Estrutura do App

```
web/
├── models.py        # Modelos: Cliente, Medico, AgendamentoConsulta
├── views.py         # Views de listagem, cadastro, exclusão e status
├── forms.py         # Formulários com validações personalizadas
├── urls.py          # Rotas do app
├── admin.py         # Registro dos modelos no Django Admin
└── templates/
    ├── base.html
    ├── login.html
    ├── pag_inicio.html
    ├── lista_de_clientes.html
    ├── lista_de_medicos.html
    ├── lista_de_consultas.html
    ├── agendar_consulta.html
    ├── add_paciente_modal.html
    └── add_medico_modal.html
```

---

## 🔒 Rotas Principais

| Rota | Descrição |
|---|---|
| `/login/` | Página de login |
| `/` | Página inicial |
| `/pacientes/` | Lista de pacientes |
| `/medicos/` | Lista de médicos |
| `/consultas/` | Lista de consultas |
| `/agendar_consulta/` | Agendamento de nova consulta |
| `/admin/` | Painel administrativo do Django |
