# Estructura de Carpetas utilizando Screaming Architecture en React

## Introducción

Este documento describe la estructura de carpetas que se seguirá en un proyecto React utilizando los principios de **Screaming Architecture**. El objetivo es organizar el código de manera que refleje claramente el dominio y la funcionalidad del sistema, facilitando su comprensión y mantenimiento.

## Estructura General

En lugar de organizar el proyecto por tipos de archivos (componentes, servicios, etc.), se hará por funcionalidades o módulos de dominio. Cada módulo contendrá todos los elementos necesarios para implementar esa parte específica del sistema.

### Estructura de Carpetas

```plaintext
src/
├── tasks/
│   ├── components/
│   │   ├── TaskList.js
│   │   └── TaskItem.js
│   ├── services/
│   │   └── TaskService.js
│   ├── hooks/
│   │   └── useTasks.js
│   ├── context/
│   │   └── TaskContext.js
│   └── utils/
│       └── taskUtils.js
├── users/
│   ├── components/
│   │   ├── UserProfile.js
│   │   └── UserList.js
│   ├── services/
│   │   └── UserService.js
│   ├── hooks/
│   │   └── useUsers.js
│   ├── context/
│   │   └── UserContext.js
│   └── utils/
│       └── userUtils.js
├── shared/
│   ├── components/
│   │   └── Button.js
│   ├── hooks/
│   │   └── useAuth.js
│   └── utils/
│       └── dateUtils.js
└── App.js

### Descripción de Carpetas y Archivos

- **`src/`**: Contiene todo el código fuente de la aplicación.

#### Módulos de Dominio

- **`tasks/`**: Este módulo gestiona todo lo relacionado con las tareas.
  - **`components/`**: Componentes específicos del módulo de tareas, como la lista de tareas (`TaskList.js`) y cada tarea individual (`TaskItem.js`).
  - **`services/`**: Servicios que interactúan con APIs u otras fuentes de datos relacionadas con tareas.
  - **`hooks/`**: Hooks personalizados que encapsulan la lógica específica de tareas.
  - **`context/`**: Contextos de React para manejar el estado global relacionado con tareas.
  - **`utils/`**: Funciones de utilidad específicas para la manipulación de tareas.

- **`users/`**: Este módulo gestiona todo lo relacionado con los usuarios.
  - **`components/`**: Componentes específicos del módulo de usuarios, como el perfil de usuario (`UserProfile.js`) y la lista de usuarios (`UserList.js`).
  - **`services/`**: Servicios que interactúan con APIs u otras fuentes de datos relacionadas con usuarios.
  - **`hooks/`**: Hooks personalizados que encapsulan la lógica específica de usuarios.
  - **`context/`**: Contextos de React para manejar el estado global relacionado con usuarios.
  - **`utils/`**: Funciones de utilidad específicas para la manipulación de usuarios.

#### Componentes y Funcionalidades Compartidas

- **`shared/`**: Contiene componentes, hooks y utilidades que se utilizan en múltiples módulos de dominio.
  - **`components/`**: Componentes reutilizables en diferentes partes de la aplicación, como `Button.js`.
  - **`hooks/`**: Hooks que pueden ser utilizados por varios módulos, como `useAuth.js`.
  - **`utils/`**: Funciones de utilidad compartidas, como `dateUtils.js`.

### Archivo Principal

- **`App.js`**: Componente raíz de la aplicación, donde se integran y configuran los distintos módulos de dominio.
