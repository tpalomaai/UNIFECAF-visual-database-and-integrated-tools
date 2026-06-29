# 🌱 Sistema Visual de Gestão — ONG Vida Plena

> Banco de Dados Visual e Ferramentas Integradas
> Projeto desenvolvido por **Paloma Ai Tsuchinaga**
> Faculdade de Inteligência Artificial — UniFECAF | 2026

---

## 🔗 Links do Projeto

| Recurso | Link |
|---|---|
| 🎥 **Vídeo Pitch (Google Drive)** | [drive.google.com/file/d/1i_vfQhVTg7zbFasVDw5pcHNgUOvq6uRL/view?usp=sharing](https://drive.google.com/file/d/1i_vfQhVTg7zbFasVDw5pcHNgUOvq6uRL/view?usp=sharing) |
| 📊 **Acesso à Base (Airtable)** | [airtable.com/appm0JuXjjy6peAjt/pag0s71jlfWt1AnCW](https://airtable.com/appm0JuXjjy6peAjt/pag0s71jlfWt1AnCW) |
| 💻 **Repositório (GitHub)** | [github.com/tpalomaai/UNIFECAF-visual-database-and-integrated-tools](https://github.com/tpalomaai/UNIFECAF-visual-database-and-integrated-tools) |

---

## 📌 Sobre o Projeto

A **ONG Vida Plena** realiza eventos sociais, ações de inclusão digital, capacitações e campanhas comunitárias. O principal desafio identificado foi a **dificuldade de organizar informações** sobre eventos, beneficiários e participações, já que o controle era feito apenas por planilhas soltas e mensagens em grupos.

Para resolver esse problema, foram definidos os seguintes requisitos principais:

- ✅ Cadastrar eventos
- ✅ Registrar beneficiários
- ✅ Acompanhar inscrições
- ✅ Visualizar o histórico de participação
- ✅ Automatizar lembretes por e-mail

---

## 🛠️ Ferramenta Utilizada

O sistema foi construído no **Airtable**, utilizando recursos **No-Code** para criar:

- Base de dados visual e relacional;
- Interfaces de navegação;
- Formulários de cadastro;
- Painel de acompanhamento (dashboard);
- Automação de notificações.

A escolha do Airtable se deu pela possibilidade de transformar dados em uma **aplicação visual simples**, sem depender de programação tradicional — o que se encaixa na realidade da ONG, que precisa de uma solução fácil de usar, manter e atualizar.

---

## 🗂️ Estrutura do Banco de Dados

O banco foi organizado em **quatro tabelas principais**:

### 1. 📅 Eventos
Reúne os dados de cada ação realizada pela ONG:
- Nome do evento
- Data
- Localização
- Capacidade
- Status
- Notas

### 2. 👤 Beneficiários
Concentra as informações das pessoas atendidas:
- Nome
- Idade
- Telefone
- E-mail
- Região
- Histórico

### 3. 🔗 Envolvidos
Tabela responsável por **Conectar Eventos e Beneficiários**, já que um evento pode ter vários participantes e um beneficiário pode participar de vários eventos. Registra:
- Status de atendimento
- Data da inscrição
- Notas
- Controle de notificação

### 4. 🧑‍💼 Responsáveis
Guarda as informações de contato das pessoas responsáveis por cada evento.

---

## 🔄 Fluxo Relacional do Sistema

```
Beneficiário cadastrado
        ↓
Registro em Envolvidos
        ↓
Vinculação com Evento
        ↓
Histórico de participação atualizado
```

Essa estrutura evita a **repetição de dados** e permite acompanhar com clareza quem participou de cada ação da ONG.

---

## 🖥️ Funcionalidades e Visualizações

O sistema conta com as seguintes interfaces, criadas para facilitar o uso por toda a equipe da ONG:

| Interface | Função |
|---|---|
| 📊 **Painel de Visão Geral** | Dashboard básico com indicadores sobre eventos, beneficiários, inscrições e status |
| 📋 **Informações de Eventos** | Visualização detalhada de cada evento cadastrado |
| 👥 **Informações de Beneficiários** | Visualização detalhada de cada beneficiário cadastrado |
| 📈 **Relatório de Envolvimento dos Beneficiários** | Histórico de participação por pessoa |
| 📝 **Formulário de Novo Evento** | Cadastro de novos eventos |
| 📝 **Formulário de Novo Beneficiário** | Cadastro de novos beneficiários |
| 📝 **Formulário de Nova Inscrição no Evento** | Vinculação de um beneficiário a um evento |

### ⏰ Automação de Lembrete por E-mail
Foi criada uma automação que utiliza os dados da tabela **Envolvidos** para:
1. Enviar uma notificação por e-mail relacionada ao evento;
2. Atualizar automaticamente o status do lembrete após o envio.

---

## 📖 Instruções de Uso

### Acessando o sistema
1. Clique no link de acesso ao Airtable disponível na seção [Links do Projeto](#-links-do-projeto).
2. Você será direcionado ao **Painel de Visão Geral**, ponto de partida para navegar pelo sistema.

### Cadastrando um novo evento
1. Acesse a interface **Formulário de Novo Evento**.
2. Preencha os campos: nome, data, localização, capacidade, status e notas.
3. Envie o formulário — o evento aparecerá automaticamente na tabela **Eventos**.

### Cadastrando um novo beneficiário
1. Acesse a interface **Formulário de Novo Beneficiário**.
2. Preencha os campos: nome, idade, telefone, e-mail, região e histórico (se houver).
3. Envie o formulário — o beneficiário aparecerá automaticamente na tabela **Beneficiários**.

### Inscrevendo um beneficiário em um evento
1. Acesse a interface **Formulário de Nova Inscrição no Evento**.
2. Selecione o beneficiário e o evento desejado.
3. Defina o status de atendimento e a data da inscrição.
4. Envie o formulário — o registro será criado na tabela **Envolvidos**, conectando beneficiário e evento.

### Acompanhando indicadores
- Use o **Painel de Visão Geral** para visualizar indicadores gerais de eventos, beneficiários e inscrições.
- Use o **Relatório de Envolvimento dos Beneficiários** para consultar o histórico de participação de uma pessoa específica.

### Lembretes automáticos
- Os lembretes por e-mail são disparados automaticamente com base nos dados da tabela **Envolvidos**, sem necessidade de ação manual. O status do lembrete é atualizado após o envio.

---

## 🔒 Ética e Segurança da Informação

Como o sistema utiliza dados pessoais (nome, telefone, e-mail, idade e região), os seguintes cuidados foram adotados:

- As informações devem ser usadas **apenas para fins administrativos da ONG**;
- Foram incluídos somente os dados **necessários** para a gestão dos eventos, evitando excesso de informações;
- O **acesso à base deve ser restrito** às pessoas autorizadas, garantindo maior segurança e privacidade dos beneficiários.

---

## ✅ Resultado Final

O projeto resultou em uma **aplicação visual funcional no Airtable**, com:

- Banco de dados relacional;
- Formulários de cadastro;
- Interfaces de navegação;
- Dashboard básico;
- Automação por e-mail.

A solução facilita a organização das atividades da **ONG Vida Plena** e reduz a dependência de controles manuais, como planilhas e mensagens em grupos.

---

## 👩‍💻 Autoria

**Paloma Ai Tsuchinaga**
Faculdade de Inteligência Artificial — UniFECAF
2026
