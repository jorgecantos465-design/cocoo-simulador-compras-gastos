# Skill: Testing y bugs - simulador compras/gastos

## Objetivo
Cubrir regresiones en compra contado, financiada, mixta, gastos nuevos, caja y cuotas.

## Cuando usarla
Usala ante bug reportado, cambio de calculo, UI de formulario o limpieza de codigo heredado.

## Pasos obligatorios
- Reproducir con datos numericos.
- Identificar si falla UI, formato o motor.
- Probar contado, 100% financiado y parte contado.
- Revisar casos de caja insuficiente.

## Checklist antes de modificar
- Caso esperado definido.
- Test existente localizado o falta documentada.
- No se borra cobertura de inversion heredada sin plan.

## Checklist antes de finalizar
- `npm test` pasa.
- `npm run build` pasa.
- Caso manual probado.

## Errores que debe evitar
- Cambiar tests para que pasen sin validar negocio.
- Ignorar meses extendidos por cuotas.
- Confundir gasto que aumenta con gasto que disminuye.

## Comandos de verificacion
- `npm test`
- `npm run build`

## Formato de reporte final
- Bug/caso.
- Datos usados.
- Causa.
- Pruebas ejecutadas.

