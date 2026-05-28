# Skill: Arquitectura tecnica - simulador compras/gastos

## Objetivo
Separar gradualmente el producto de compras sin romper el simulador ni la logica financiera heredada.

## Cuando usarla
Usala al tocar rutas, `Simulator.tsx`, tipos, imports o estructura Next.

## Pasos obligatorios
- Revisar `src/app/page.tsx` y `src/app/simulador-compra/page.tsx`.
- Identificar ramas heredadas de inversion antes de eliminarlas.
- Mantener cambios pequenos y validados.
- No reescribir `finance.ts` sin plan y tests.

## Checklist antes de modificar
- Build actual conocido.
- Dependencias cruzadas identificadas.
- No se toca `package.json`.

## Checklist antes de finalizar
- `npm test` y `npm run build` pasan.
- No quedan rutas de inversion publicas.
- Imports sin uso removidos si aplica.

## Errores que debe evitar
- Eliminar codigo compartido usado por compras.
- Cambiar firmas de `calculate` sin actualizar tests.
- Hacer refactor grande junto con cambios visuales.

## Comandos de verificacion
- `npm test`
- `npm run build`
- `npm run lint`

## Formato de reporte final
- Estructura afectada.
- Dependencias cruzadas resueltas o pendientes.
- Validaciones.
- Riesgo residual.

