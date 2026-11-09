# 📱 Gerenciador de Tarefas - SQLite no Flutter

Projeto desenvolvido para a disciplina de **Programação para Dispositivos Móveis**, aplicando conceitos de persistência de dados local com **SQLite** (`sqflite`) em **Flutter**.

---

## 🚀 Tecnologias e Pacotes Utilizados

* **Flutter** & **Dart**[cite: 1]
* **sqflite** (^2.3.2) - Motor de banco de dados relacional local[cite: 1]
* **sqflite_common_ffi** - Suporte para execução do banco em Desktop (Windows/Linux/macOS)
* **path** (^1.9.0) - Manipulação de caminhos de diretórios[cite: 1]

---

## 📋 Funcionalidades (CRUD Completo)

O aplicativo conta com operações completas de persistência local:
* **Create (Inserir):** Adiciona novas tarefas através de um formulário interativo (*ModalBottomSheet*)[cite: 1, 4].
* **Read (Consultar):** Carrega e exibe a lista de tarefas ordenadas por ID de forma reativa (`ListView.builder`)[cite: 1, 5].
* **Update (Atualizar):** Permite marcar tarefas como concluídas (com efeito visual de risco no texto) ou editar suas informações[cite: 1, 4, 5].
* **Delete (Excluir):** Remove permanentemente a tarefa do banco de dados através do botão de lixeira[cite: 1, 5].

---

## 🗂️ Estrutura do Projeto

```text
lib/
│
├── database/
│   └── database_helper.dart   # Gerenciador Singleton e comandos SQL (CRUD)[cite: 1, 3]
│
├── models/
│   └── tarefa_model.dart      # Modelo de dados com toMap() e fromMap()[cite: 1, 2]
│
├── screens/
│   └── tarefas_screen.dart    # Interface principal reativa, modais e lista[cite: 1, 4, 5]
│
└── main.dart                  # Configuração inicial e tema do aplicativo[cite: 5]
