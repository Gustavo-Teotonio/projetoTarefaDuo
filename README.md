# 📋 Sistema de Gerenciamento de Tarefas

Um sistema completo de gerenciamento de tarefas desenvolvido seguindo o padrão MVC (Model-View-Controller) com Node.js, Express, Handlebars e Sequelize.

## 🚀 Funcionalidades Implementadas

### ✅ Funcionalidades Básicas

- **CRUD Completo**: Criar, visualizar, editar e excluir tarefas
- **Status de Tarefas**: Marcar tarefas como concluídas ou pendentes
- **Interface Responsiva**: Design moderno e adaptável a diferentes dispositivos

### 🎯 Funcionalidades Avançadas (Desafio Final)

#### 1. **Sistema de Prioridades**

- **Níveis**: Baixa, Média e Alta
- **Visualização**: Cores diferenciadas por prioridade
- **Padrão**: Média (definida automaticamente)

#### 2. **Data de Entrega**

- **Campo Opcional**: Data limite para conclusão da tarefa
- **Visualização**: Ícone de calendário com a data
- **Formato**: YYYY-MM-DD

#### 3. **Filtros Inteligentes**

- **Por Status**: Todas, Pendentes, Concluídas
- **Por Prioridade**: Todas, Baixa, Média, Alta
- **Combinados**: Filtros funcionam simultaneamente

#### 4. **Estilização por Prioridade**

- **Baixa**: Verde (#28a745)
- **Média**: Amarelo (#ffc107)
- **Alta**: Vermelho (#dc3545)
- **Efeitos**: Bordas coloridas e badges diferenciadas

## 🏗️ Arquitetura MVC

### **Model** (`models/Task.js`)

```javascript
// Estrutura da tarefa
{
  title: String (obrigatório),
  description: String,
  done: Boolean (padrão: false),
  priority: ENUM('Baixa', 'Média', 'Alta') (padrão: 'Média'),
  dueDate: DATEONLY (opcional)
}
```

### **View** (`views/`)

- **create.handlebars**: Formulário de criação com todos os campos
- **edit.handlebars**: Formulário de edição com valores pré-preenchidos
- **all.handlebars**: Lista com filtros e estilização por prioridade
- **main.handlebars**: Layout principal com navegação

### **Controller** (`controllers/taskController.js`)

- **showTasks**: Exibe todas as tarefas
- **createTask**: Renderiza formulário de criação
- **saveTask**: Salva nova tarefa no banco
- **editTask**: Renderiza formulário de edição
- **updateTask**: Atualiza tarefa existente
- **deleteTask**: Remove tarefa do banco

## 🎨 Estilos CSS

### **Arquivo**: `public/css/styles.css`

- **Design Moderno**: Interface limpa e profissional
- **Cores por Prioridade**: Sistema visual intuitivo
- **Responsividade**: Adaptável a mobile e desktop
- **Animações**: Transições suaves e efeitos hover
- **Acessibilidade**: Contraste adequado e navegação clara

## 🔧 Tecnologias Utilizadas

- **Backend**: Node.js + Express.js
- **Template Engine**: Handlebars
- **Banco de Dados**: SQLite (via Sequelize)
- **Frontend**: HTML5 + CSS3 + JavaScript
- **Padrão**: MVC (Model-View-Controller)

## 📁 Estrutura do Projeto

```
projetoTarefaDuo/
├── controllers/
│   └── taskController.js
├── db/
│   └── conn.js
├── models/
│   └── Task.js
├── routes/
│   └── taskRoutes.js
├── views/
│   ├── all.handlebars
│   ├── create.handlebars
│   ├── edit.handlebars
│   └── main.handlebars
├── public/
│   └── css/
│       └── styles.css
├── index.js
└── package.json
```

## 🚀 Como Executar

1. **Instalar dependências**:

   ```bash
   npm install
   ```

2. **Executar o servidor**:

   ```bash
   npm start
   ```

3. **Acessar a aplicação**:
   ```
   http://localhost:3000
   ```

## 🎯 Funcionalidades dos Filtros

### **Filtro por Status**

- **Todas**: Mostra todas as tarefas
- **Pendentes**: Apenas tarefas não concluídas
- **Concluídas**: Apenas tarefas finalizadas

### **Filtro por Prioridade**

- **Todas**: Mostra todas as prioridades
- **Baixa**: Tarefas de baixa prioridade
- **Média**: Tarefas de média prioridade
- **Alta**: Tarefas de alta prioridade

### **Filtros Combinados**

Os filtros funcionam simultaneamente, permitindo combinações como:

- "Pendentes de Alta Prioridade"
- "Concluídas de Baixa Prioridade"

## 🎨 Sistema de Cores

| Prioridade | Cor da Borda | Cor do Badge   | Significado       |
| ---------- | ------------ | -------------- | ----------------- |
| **Baixa**  | Verde        | Verde claro    | Sem urgência      |
| **Média**  | Amarelo      | Amarelo claro  | Prioridade normal |
| **Alta**   | Vermelho     | Vermelho claro | Urgente           |

## 📝 Exemplo de Uso

1. **Criar Tarefa**: Acesse "Criar Nova Tarefa"
2. **Definir Prioridade**: Escolha entre Baixa, Média ou Alta
3. **Definir Data**: Adicione uma data de entrega (opcional)
4. **Filtrar**: Use os filtros para organizar suas tarefas
5. **Editar**: Clique em "Editar" para modificar qualquer tarefa
6. **Concluir**: Marque como concluída quando finalizar

## 🏆 Desafios Implementados

✅ **Nível de Prioridade**: Sistema completo com 3 níveis  
✅ **Estilização por Prioridade**: Cores e badges diferenciadas  
✅ **Data de Entrega**: Campo opcional com visualização  
✅ **Filtro de Tarefas**: Por status e prioridade  
✅ **Interface Moderna**: Design responsivo e profissional

---

**Desenvolvido seguindo o padrão MVC** 🎯  
**Interface moderna e intuitiva** 🎨  
**Funcionalidades completas** ⚡

