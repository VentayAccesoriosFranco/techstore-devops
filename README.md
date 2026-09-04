# TechStore DevOps - Proyecto Inicial

## Contexto

TechStore GT posee una aplicación pequeña que necesita ser modernizada utilizando prácticas DevOps.

El proyecto contiene intencionalmente algunos problemas que deberán ser identificados y corregidos durante la práctica.

## Requisitos

- Node.js 20 o superior
- Git
- Cuenta de GitHub
- Acceso a Azure DevOps
- Visual Studio Code, IntelliJ IDEA u otro editor

## Instalación

```bash
npm install
```

## Ejecutar aplicación

```bash
npm start
```

## Ejecutar pruebas

```bash
npm test
```

## Estructura

```text
techstore-devops/
├── config/
│   └── config.js
├── docs/
├── src/
│   ├── app.js
│   └── demo.js
├── tests/
│   └── app.test.js
├── .gitignore
├── package.json
└── README.md
```

## Importante

No modifique el proyecto antes de iniciar la práctica.

Durante la actividad deberá analizar su estructura, identificar problemas y aplicar las prácticas DevOps indicadas por el docente.

## Integración Continua (CI)

Este proyecto cuenta con un pipeline automatizado de Integración Continua utilizando **GitHub Actions**.

- **Workflow:** `.github/workflows/ci.yml`
- **Gatillo (Triggers):** Se ejecuta automáticamente en cada `push` o `pull request` hacia la rama `main`.
- **Acciones:**
  - Despliega un entorno virtual aislado (`ubuntu-latest`).
  - Instala las dependencias del proyecto (`npm install`).
  - Ejecuta la suite de pruebas unitarias (`npm test`).

## Flujo de Trabajo y Revisiones de Código (Code Review)

Para garantizar la calidad del código y la estabilidad del sistema:

1. Queda restringido el envío directo de commits a la rama `main`.
2. Todo nuevo desarrollo o corrección se realiza en ramas secundarias (`feature/*` o `fix/*`).
3. Los cambios se integran a `main` únicamente mediante **Pull Requests (PR)** previa aprobación y ejecución exitosa del pipeline de CI.
