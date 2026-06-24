# Sistema Clínico — Clínica Long Life

Sistema web para gestão de agendamentos de consultas médicas, controle de pacientes e médicos em clínicas.

---

## 👥 Integrantes

- Geovanna Alves Rodrigues
- Luan Matos
- Lucas Kauan
- José Carlos
- Natanael Reis

---

## 🎯 Objetivo

Otimizar processos administrativos de clínicas médicas, reduzindo erros de agendamento e facilitando o controle de pacientes, médicos e consultas por meio de uma interface web intuitiva.

---

## ⚙️ Principais Funcionalidades

- **Autenticação** — login e logout com controle de acesso por sessão
- **Cadastro de pacientes** — com validação de CPF (formato `000.000.000-00`), nome completo, telefone e data de nascimento (mínimo 6 anos)
- **Cadastro de médicos** — com validação de CRM (formato `CRM/UF 000000`), especialidade e horário de atendimento
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
- **Bootstrap 5** — estilização e componentes (modais, tabelas, alertas)
- **jQuery** + **AJAX** — submissão de formulários sem recarregar a página
- **FullCalendar 6** — exibição do calendário de consultas
- **SQLite** (padrão Django) — banco de dados

---

## 📁 Estrutura do App (`web/`)

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

## 🚀 Como Executar

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
   ```

2. **Crie e ative um ambiente virtual:**
   ```bash
   python -m venv venv
   source venv/bin/activate      # Linux/Mac
   venv\Scripts\activate         # Windows
   ```

3. **Instale as dependências:**
   ```bash
   pip install django
   ```

4. **Execute as migrações:**
   ```bash
   python manage.py migrate
   ```

5. **Crie um superusuário:**
   ```bash
   python manage.py createsuperuser
   ```

6. **Inicie o servidor:**
   ```bash
   python manage.py runserver
   ```

7. **Acesse no navegador:** `http://127.0.0.1:8000/`

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
