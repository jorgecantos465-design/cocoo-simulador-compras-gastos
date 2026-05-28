# AGENTS.md - cocoo-simulador-compras-gastos

## Objetivo del proyecto

Web app simple de Cocoo para evaluar si una persona puede sostener una compra o gasto importante antes de tomar la decision, mostrando impacto en caja, financiamiento y escenarios.

## Stack tecnico detectado

- Next.js 16 App Router
- React 19
- TypeScript
- Tailwind CSS 4 via `@tailwindcss/postcss`
- Vitest para pruebas de librerias
- Calculos 100% frontend, sin login ni base de datos

## Comandos

- Instalacion: `npm install`
- Desarrollo: `npm run dev`
- Test: `npm test`
- Build: `npm run build`
- Start produccion: `npm start`
- Lint: `npm run lint` (script existe; verificar compatibilidad de Next 16 si falla)

## Estructura y archivos criticos

- `src/app/page.tsx`: redirect a `/simulador-compra`.
- `src/app/simulador-compra/page.tsx`: ruta principal del producto.
- `src/components/Simulator.tsx`: UI y flujo del simulador; todavia conserva ramas compartidas heredadas.
- `src/lib/finance.ts`: motor de calculo financiero compartido heredado.
- `src/lib/finance.test.ts`: tests de calculos, actualmente cubren compras e inversiones.
- `src/lib/format.ts`: parseo y formato de importes.
- `src/app/globals.css`: variables y estilos globales.

## Reglas de trabajo

- No tocar `node_modules`, `.next`, `dist` ni `build`.
- No cambiar `package.json` o lockfile sin avisar antes.
- No reescribir formulas financieras sin casos esperados y tests.
- Mantener la ruta publica principal en `/simulador-compra`.
- Si se elimina codigo heredado de inversiones, hacerlo en pasos chicos y con `npm test` + `npm run build`.
- Mantener experiencia sin backend, login, pagos ni descargas salvo autorizacion.

## No tocar sin autorizacion

- Semantica de `calculate`, `Inputs`, cuotas y estados de riesgo.
- Casos de `finance.test.ts` hasta que se separen por dominio.
- Redirect de `src/app/page.tsx`.
- Textos legales o disclaimers si se agregan.

## Estrategia de commits

- Primeros commits recomendados: limpieza de ruta/ramas no usadas, luego separacion de tests.
- Separar UI de cambios en motor financiero.
- Todo cambio de calculo debe incluir o actualizar tests.

## Criterios de finalizacion

- `npm test` pasa.
- `npm run build` pasa.
- Build solo expone `/` y `/simulador-compra` como rutas funcionales del producto.
- Flujo de compra contado, financiado y mixto funciona manualmente.

## Subagentes recomendados

Antes de activar un rol, revisar el indice operativo en `skills/README.md`.

- Roadmap y negocio: usar `skills/roadmap-negocio.md`.
- Arquitectura tecnica: usar `skills/arquitectura-tecnica.md`.
- Motor matematico / logica de negocio: usar `skills/motor-matematico-logica.md`.
- Frontend UI: usar `skills/frontend-ui.md`.
- UX y flujo: usar `skills/ux-flujo.md`.
- Testing y bugs: usar `skills/testing-bugs.md`.
