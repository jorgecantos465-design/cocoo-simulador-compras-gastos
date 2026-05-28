# Skill: Motor matematico / logica - simulador compras/gastos

## Objetivo
Proteger calculos de sostenibilidad: caja, excedente mensual, cuotas, pago inicial y estres financiero.

## Cuando usarla
Usala al tocar `src/lib/finance.ts`, escenarios, estados o calculos derivados en `Simulator.tsx`.

## Pasos obligatorios
- Crear casos numericos antes de cambiar.
- Separar flujo actual de impacto incremental.
- Validar contado, financiado y mixto.
- Verificar meses de analisis versus meses de cuotas.

## Checklist antes de modificar
- Formula actual entendida.
- Tests relevantes ubicados.
- Resultado esperado calculado manualmente.

## Checklist antes de finalizar
- `npm test` pasa.
- No hay `NaN` ni valores infinitos.
- Estados `Sostenible`, `Ajustada`, `Riesgo alto` siguen defendibles.

## Errores que debe evitar
- Restar capital financiado dos veces.
- Ignorar gastos nuevos negativos.
- Redondear antes de terminar calculos.

## Comandos de verificacion
- `npm test`
- `npm run build`

## Formato de reporte final
- Formula tocada.
- Casos numericos.
- Resultados antes/despues.
- Cobertura de tests.

