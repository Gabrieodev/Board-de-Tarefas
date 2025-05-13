# 🗂️ Board de Gerenciamento de Tarefas

Este projeto é um **Board customizável** para gerenciamento de tarefas desenvolvido em **Java** no **Visual Studio Code**, com persistência dos dados utilizando **MySQL**. Ele permite o acompanhamento completo do ciclo de vida de tarefas por meio de cards organizados em colunas específicas.

## 🚀 Funcionalidades Principais

- Menu inicial com as opções:
  - Criar novo board
  - Selecionar board
  - Excluir boards
  - Sair
- Cada board possui:
  - Nome identificador
  - No mínimo 3 colunas:
    - Inicial (primeira)
    - Final (penúltima)
    - Cancelamento (última)
    - Colunas pendentes opcionais (entre inicial e final)
- Cards:
  - Criar, mover, cancelar, bloquear e desbloquear
  - Só podem ser movidos em sequência, exceto para a coluna de cancelamento
  - Bloqueio/desbloqueio exige motivo

## 📋 Regras de Negócio

### Colunas
- Cada board pode conter:
  - 1 coluna **Inicial**
  - 1 coluna **Final**
  - 1 coluna **Cancelamento**
  - N colunas do tipo **Pendente**
- Ordem obrigatória:
  - Inicial → [Pendentes] → Final → Cancelamento

### Cards
- Atributos:
  - Título
  - Descrição
  - Data de criação
  - Estado de bloqueio (com motivo)
- Bloqueados não podem ser movidos
- Podem ser cancelados de qualquer coluna, exceto a final
- Transição entre colunas obrigatoriamente em sequência

## 📊 Funcionalidades Extras (Implementadas)

- Registro de **data/hora** ao entrar e sair de cada coluna
- **Relatório de tempo** por tarefa:
  - Tempo total para conclusão
  - Tempo gasto em cada coluna
- **Relatório de bloqueios**:
  - Motivos de bloqueio/desbloqueio
  - Tempo total bloqueado

## 💾 Tecnologias Utilizadas

- **Linguagem:** Java
- **IDE:** Visual Studio Code
- **Banco de Dados:** MySQL

## 🙏 Agradecimentos

Projeto desenvolvido por [Gabrieodev](https://github.com/Gabrieodev) como forma de praticar e aplicar conhecimentos em Java e banco de dados.  
Agradeço à [DIO (Digital Innovation One)](https://www.dio.me) pela proposta do desafio e pela oportunidade de aprendizado contínuo.
