## Exercício: TODO List com Vue (Front-end only)
#### Criar uma aplicação simples de lista de tarefas (TODO List) que permita:
- Adicionar novas tarefas
- Marcar/desmarcar tarefas como concluídas
- Remover tarefas
- Filtrar tarefas (Todas | Ativas | Concluídas)
- Persistir no localStorage (opcional extra)

#### Requisitos de Ferramentas
	- Vite (para criar e rodar o projeto)
	- Vue 3 (composition ou options API, escolha)
#
#### 1. Criar projeto
	- npm create vite@latest vue-todos
	- cd name
	- npm install
	- npm run dev

#### 2. Estrutura sugerida
```
	src/
 	├─ components/
 	│   ├─ TodoInput.vue
 	│   ├─ TodoItem.vue
 	│   └─ TodoList.vue
 	├─ App.vue
 	└─ main.js
```

#### 3. Funcionalidades (o que praticar)

- App.vue
    - Responsável por controlar o estado principal (lista de todos).
    - Passa os dados para TodoList.vue.
    - Recebe eventos do TodoInput.vue e TodoItem.vue.
- TodoInput.vue
    - Input + botão para adicionar tarefa.
    - Emite evento add-todo para o App.
- TodoItem.vue
    - Renderiza cada tarefa individual.
    - Permite marcar como concluída (checkbox).
    - Botão para remover.
    - Usa props para receber dados e emit para ações.
- TodoList.vue
    - Recebe a lista de tarefas via props.
    - Itera sobre elas e renderiza TodoItem.
    - Emite eventos para o App quando tarefa é removida ou concluída.

#### 4. Extras (desafio)
- Adicionar filtro: mostrar somente Todas | Ativas | Concluídas.
- Usar computed para calcular quantas tarefas ainda faltam.
- Persistir no localStorage para não perder os dados ao recarregar.
