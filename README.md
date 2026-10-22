# Buscador de Usuarios de GitHub

Una aplicación web moderna y reactiva desarrollada con **React 19**, **TypeScript** y **Vite**, diseñada bajo una estética **minimalista y sofisticada** inspirada en los estándares de diseño de Apple, con acentos en azul zafiro y soporte modular.

---

## Características Principales

- **Diseño Minimalista & Sofisticado:**
  - Tipografía cuidada con las fuentes *Plus Jakarta Sans* e *Inter*.
  - Paleta de colores balanceada con acentos zafiro, sombras multi-capa sutiles y micro-interacciones suaves.
  - Diseño responsivo adaptado para escritorio y dispositivos móviles.
- **Búsqueda en Tiempo Real:**
  - Barra de búsqueda optimizada con soporte para tecla `Enter`, validación y estados de carga animados.
  - Desacoplamiento de la lógica mediante el hook personalizado `useSearchBar`.
- **Lista Dinámica de Resultados:**
  - Consulta a la API pública de GitHub (`/search/users`).
  - Tarjetas interactivas con avatar, nombre de usuario y badge de tipo de cuenta.
  - Resaltado visual instantáneo del usuario activo seleccionado.
- **Panel de Inspección de Usuario:**
  - Consulta detallada mediante `useUserInfo` (`/users/{username}`).
  - Tarjeta *sticky* con avatar ampliado, biografía, enlaces a blog/sitio, compañía y ubicación.
  - Métricas destacadas: **Repositorios públicos**, **Seguidores** y **Seguidos**.
  - Enlace directo al perfil oficial en GitHub con navegación segura (`rel="noopener noreferrer"`).
- **Código Limpio & Tipado Fuerte:**
  - Componentes modulares utilizando **CSS Modules**.
  - Tipos TypeScript estrictos para respuestas de API y modelos de datos.

---

## Tecnologías Utilizadas

- **Framework:** [React 19](https://react.dev/)
- **Lenguaje:** [TypeScript](https://www.typescriptlang.org/)
- **Entorno de desarrollo & Bundler:** [Vite](https://vitejs.dev/)
- **Estilos:** CSS Modules & Vanilla CSS con Custom Properties (CSS Variables)
- **Fuentes:** Google Fonts (*Plus Jakarta Sans* & *Inter*)
- **API:** [GitHub REST API](https://docs.github.com/en/rest)

---

## Estructura del Proyecto

```text
Manejo_de_inputs/
├── GithubAPI_Bruno/         # Colección de peticiones para Bruno
├── GithubAPI_POSTMAN.json   # Colección de peticiones para Postman
├── GithubAPI_YAML.yml       # Especificación OpenAPI / Bruno YAML
├── src/
│   ├── components/
│   │   ├── Results/
│   │   │   ├── ResultItem.tsx          # Componente de tarjeta de usuario en resultados
│   │   │   ├── ResultSetWrapper.tsx    # Contenedor de la lista de resultados
│   │   │   └── results.module.css      # Estilos modulares de resultados
│   │   ├── SearchBar/
│   │   │   ├── SearchBar.tsx           # Input y botón de búsqueda
│   │   │   └── SearchBar.module.css    # Estilos del formulario de búsqueda
│   │   └── UserInfo/
│   │       ├── UserInfo.tsx            # Ficha con información extendida del usuario
│   │       └── UserInfo.module.css     # Estilos de la tarjeta de detalle
│   ├── hooks/
│   │   ├── useSearchBar.ts             # Manejo de estado del input de búsqueda
│   │   ├── useSearchUser.ts            # Peticiones y estados para búsqueda de usuarios
│   │   └── useUserInfo.ts              # Consulta de información detallada de perfil
│   ├── types/
│   │   └── github.ts                   # Interfaces y contratos de tipos de GitHub
│   ├── App.module.css                  # Layout general y estados globales
│   ├── App.tsx                         # Componente principal y orquestación de vistas
│   ├── index.css                       # Variables CSS globales y reset de estilos
│   └── main.tsx                        # Punto de entrada de la aplicación
├── index.html                          # Plantilla HTML base y fuentes
├── package.json                        # Dependencias y scripts
├── tsconfig.json                       # Configuración de TypeScript
└── vite.config.js                      # Configuración de Vite
```

---

## Instalación y Puesta en Marcha

1. **Clonar o situarse en el directorio del proyecto:**
   ```bash
   cd Manejo_de_inputs
   ```

2. **Instalar dependencias:**
   ```bash
   npm install
   ```

3. **Ejecutar en entorno de desarrollo:**
   ```bash
   npm run dev
   ```

4. **Compilar para producción:**
   ```bash
   npm run build
   ```

---

## Pruebas de API (Colecciones Incluidas)

Para probar los endpoints utilizados de la API de GitHub de forma independiente:
- **Bruno:** Carpeta `GithubAPI_Bruno/`
- **Postman:** Archivo `GithubAPI_POSTMAN.json`
- **OpenAPI / YAML:** Archivo `GithubAPI_YAML.yml`
