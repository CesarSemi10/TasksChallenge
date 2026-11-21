# Tasks Challenge – Frontend

Aplicación móvil desarrollada con **React Native y TypeScript**, utilizando Expo. El proyecto permite gestionar tareas y consultar una lista de elementos obtenidos desde una API REST.

## Tecnologías utilizadas

- **React Native:** desarrollo de la aplicación móvil.
- **Expo:** entorno de desarrollo y ejecución.
- **TypeScript:** tipado estático.
- **Redux Toolkit:** administración del estado global de las tareas.
- **React Redux:** integración de Redux con React Native.
- **React Navigation:** navegación entre pantallas.
- **Axios:** consumo de servicios HTTP.
- **Jest:** ejecución de pruebas unitarias.
- **React Native Testing Library:** pruebas de componentes e interacciones.

## Funcionalidades

### 1. Pantalla principal

- Pantalla de inicio de la aplicación.
- Navegación hacia las secciones de tareas y listado de elementos.

### 2. Gestión de tareas

- Visualización de las tareas registradas.
- Registro de nuevas tareas mediante un modal.
- Validación para impedir el registro de descripciones vacías.
- Marcado de tareas como completadas.
- Eliminación de tareas.
- Persistencia del estado mientras se navega entre las pantallas, mediante Redux Toolkit.

### 3. Listado de elementos

- Consumo de una API REST.
- Obtención de información desde el siguiente endpoint:

  `https://6172cfe5110a740017222e2b.mockapi.io/elements`

- Visualización de los elementos obtenidos.
- Indicador de carga durante la consulta.

## Requisitos previos

Antes de ejecutar el proyecto, asegúrate de tener instalado:

- Node.js
- npm
- Expo CLI (se puede utilizar mediante `npx`)
- Expo Go en un dispositivo Android o iOS, si deseas probar la aplicación en un dispositivo físico.

## Instalación

Clona el repositorio y accede a la carpeta del proyecto:

```bash
git clone <URL_DEL_REPOSITORIO>
cd TasksChallenge
```

Instala las dependencias:

```bash
npm install
```

## Ejecución

Inicia el servidor de desarrollo de Expo:

```bash
npx expo start
```

Escanea el código QR desde la aplicación Expo Go para ejecutar el proyecto en tu dispositivo móvil.

También puedes utilizar:

```bash
npx expo start --android
```

## Pruebas unitarias

Para ejecutar las pruebas:

```bash
npm test
```

Para ejecutar las pruebas en modo de observación:

```bash
npm test -- --watch
```

Las pruebas contemplan:

- Componentes de la pantalla de tareas.
- Operaciones del estado global de Redux.
- Servicio de consulta de elementos.
- Pantalla de listado de elementos.
- Validaciones e interacciones de usuario.

## Arquitectura y organización

El proyecto organiza sus responsabilidades por funcionalidades:

```text
src/
├── components/
├── navigation/
├── screens/
│   ├── HomeScreen.tsx
│   ├── TasksScreen.tsx
│   └── ListScreen.tsx
├── services/
│   └── elementsService.ts
├── store/
│   ├── tasks/
│   │   └── tasksSlice.ts
│   ├── hooks.ts
│   └── store.ts
└── __tests__/
```

*Nota: la estructura es referencial y debe ajustarse a las carpetas y archivos reales del repositorio.*

## Administración del estado

Redux Toolkit se utiliza para centralizar la gestión de tareas.

Las principales operaciones implementadas son:

- `addTask`: agrega una nueva tarea.
- `removeTask`: elimina una tarea.
- `toggleTask`: cambia el estado de una tarea entre pendiente y completada.

## Autor

Desarrollado **César Seminario Gómez** como parte del desafío técnico de **Coderland**.

---

**Proyecto:** Tasks Challenge  
**Frontend:** React Native + TypeScript  
**Entorno:** Expo