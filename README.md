# Dashboard de Contactos — React + TypeScript

Panel de contactos hecho con **React**, **TypeScript** y **Bootstrap**, creado con **Vite**.
Es la misma práctica que el `dashboard-app` de Angular, ahora con React.

Taller de la materia **Programación Web en el Cliente**, UEES.
**Autora:** Paula Martillo Quintana

## Qué hace

Muestra una tabla de Bootstrap con una lista de contactos (id, nombre y email).
Por ahora los datos están fijos en el código. En la Clase 2 se van a traer desde una API.

## Tecnologías

- React 19 + TypeScript
- Vite
- Bootstrap 5

## Estructura

```
src/
├── components/
│   ├── ContactList.tsx   # Componente padre: tiene la lista y arma la tabla
│   └── ContactRow.tsx    # Componente hijo: dibuja una fila por contacto
├── types/
│   └── contact.ts        # Interfaz Contact (id, name, email)
├── App.tsx               # Componente raíz: título + <ContactList />
└── main.tsx              # Punto de entrada: importa Bootstrap y monta <App />
```

## Conceptos practicados

- **Componentes funcionales:** cada componente es una función que devuelve JSX.
- **Props:** `ContactList` le pasa cada contacto a `ContactRow` (`contact={contact}`), como un `input()` en Angular.
- **Listas con `map()` y `key`:** reemplaza al `@for (...; track contact.id)` de Angular.
- **Tipos con `import type`:** lo exige `verbatimModuleSyntax` en la plantilla de Vite.

## Cómo ejecutarlo

```bash
npm install
npm run dev
```

Luego abre `http://localhost:5173` en el navegador.
