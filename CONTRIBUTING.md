# Cómo se trabaja en Kamai-Lab

## Nomenclatura de repos

El prefijo indica el team, seguido del nombre del proyecto:

- `implementex-proyecto` — trabajo de cliente (implementex-devs)
- `implementin-proyecto` — herramientas propias de Kamai (implementin-devs)
- `vibecoding-proyecto` — experimentos, no oficial (vibecodianos)

Ejemplo: `implementex-market-research`

Siempre en minúsculas, sin espacios.

## Al crear un repo nuevo
GitHub no conecta un repo nuevo a ningún team automáticamente. Paso manual obligatorio:

1. Settings del repo → **Collaborators and teams**
2. **Add teams** → elegí el team correspondiente (`implementin-devs`, `implementex-devs`, `vibecodianos`)
3. Asigná permiso **Write**

## CODEOWNERS
Todo repo con trabajo real necesita su propio `.github/CODEOWNERS` (no se hereda desde este repo). Antes de nombrar a alguien ahí, confirmá que tiene Write explícito en ese repo puntual — sin eso, GitHub no lo pide como reviewer.

## Formato de commits

Conventional commits, spec oficial (conventionalcommits.org): `tipo(alcance): descripción`.

| Tipo | Para qué es |
|---|---|
| `feat` | Funcionalidad nueva para quien usa el software |
| `fix` | Arreglo de un bug |
| `docs` | Cambios solo de documentación (README, comentarios, este archivo) |
| `style` | Formato que no cambia el comportamiento (espacios, punto y coma, indentación) |
| `refactor` | Reordenar o limpiar código sin agregar feature ni arreglar bug |
| `perf` | Cambio enfocado en mejorar performance |
| `test` | Agregar o corregir tests, sin tocar código de producción |
| `build` | Cambios al sistema de build o dependencias externas |
| `ci` | Cambios a la configuración de CI (workflows de GitHub Actions, etc.) |
| `chore` | Tareas de mantenimiento que no entran en ninguna de las anteriores |

Ejemplos:
- `feat(conciliacion): agregar match por OCR de comprobantes`
- `fix(sms): corregir formato de telefono en el envio`
- `chore(deps): actualizar dependencias de seguridad`

El scope (lo que va entre paréntesis) es opcional, pero ayuda a ubicar rápido qué parte del proyecto tocó el commit.

## Flujo de labels en un issue
`status:needs-review` (recién creado) → `status:assigned` (tiene owner y arrancó) → `status:approved` (listo para PR).

## Templates
No se abren issues en blanco salvo que seas maintainer. Usá el template que corresponda: bug, feature, o tarea asignada.

