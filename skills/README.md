# Skills - cocoo-simulador-compras-gastos

## Indice

- `roadmap-negocio.md`: alcance del simulador de compras y gastos.
- `arquitectura-tecnica.md`: rutas, estructura Next y separacion del codigo heredado.
- `motor-matematico-logica.md`: sostenibilidad, caja, cuotas, gastos nuevos y estres financiero.
- `frontend-ui.md`: UI del simulador y resultados.
- `ux-flujo.md`: pasos, textos, ayudas y lectura del resultado.
- `testing-bugs.md`: escenarios, regresiones y validacion numerica.

## Cuando activar cada skill

- Cambios visuales: `frontend-ui.md`.
- Cambios de textos, labels o flujo: `ux-flujo.md`.
- Cambios de calculo: `motor-matematico-logica.md` + `testing-bugs.md`.
- Cambios en rutas/estructura: `arquitectura-tecnica.md`.
- Cambios de alcance del producto: `roadmap-negocio.md`.
- Bugs: `testing-bugs.md`.

## Orden recomendado si hay varias capas

1. `roadmap-negocio.md` si cambia alcance.
2. `arquitectura-tecnica.md` si cambia estructura.
3. `motor-matematico-logica.md` si hay calculos.
4. `ux-flujo.md` para textos/orden.
5. `frontend-ui.md` para visual.
6. `testing-bugs.md` siempre que haya calculo o bug.

## Matriz de riesgo

- Bajo: copy menor, estilos menores, README.
- Medio: `Simulator.tsx` visual/flujo, `globals.css`, rutas.
- Alto: `src/lib/finance.ts`, `src/lib/finance.test.ts`, semantica de cuotas/caja/estados.

## Comandos seguros

- `npm test`
- `npm run build`
- `npm run dev`

## Comandos condicionales

- `npm run lint`: solo si el tooling local de Next lo soporta.
- `npm install`: solo si faltan dependencias.

## Comandos prohibidos o que requieren confirmacion

- `npm audit fix`: requiere confirmacion.
- Cambios en `package.json` o lockfile: requieren confirmacion.
- Reescritura de `finance.ts`: requiere plan y confirmacion.

## Ownership por archivos criticos

- `src/lib/finance.ts`: Motor matematico, ownership principal.
- `src/lib/finance.test.ts`: Testing y bugs, con Motor matematico cuando cambian formulas.
- `src/components/Simulator.tsx`: Frontend UI, UX, Arquitectura; Motor solo para calculos derivados.
- `src/app/page.tsx`, `src/app/simulador-compra/page.tsx`: Arquitectura tecnica.
- `src/app/globals.css`: Frontend UI.

## Proximo desarrollo recomendado

Separar tests por dominio antes de refactorizar logica financiera.

