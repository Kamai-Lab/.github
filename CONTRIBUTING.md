# Cómo se trabaja en Kamai-Lab

## Nomenclatura de repos

El prefijo indica el team. En trabajo de cliente va también el nombre del cliente:

- `implementex-cliente-proyecto` — trabajo de cliente (implementex-devs)
- `implementin-kamai-proyecto` — producto propio de KAMAI, el cliente somos nosotros (implementin-devs)
- `vibecoding-proyecto` — experimentos, no oficial (vibecodianos)

Ejemplos:
- `implementex-laofrenda-conciliacion`
- `implementin-kamai-website`
- `vibecoding-sync-tasks`

El nombre del cliente es obligatorio: sin él no hay
forma de saber de quién es cada proyecto, ni de responder rápido si un cliente
pregunta quién tiene acceso a sus datos.

Siempre en minúsculas, sin espacios.

## Al crear un repo nuevo

Usa la plantilla `repo-template` con el botón **Use this template**. Después:

1. Settings del repo → **Collaborators and teams**
2. **Add teams** → elige el team correspondiente (`implementin-devs`, `implementex-devs`, `vibecodianos`)
3. Asigna permiso **Write**

GitHub no conecta un repo nuevo a ningún team automáticamente. Es un paso manual obligatorio.

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
- `fix(sms): corregir formato de teléfono en el envío`
- `chore(deps): actualizar dependencias de seguridad`

El scope (lo que va entre paréntesis) es opcional, pero ayuda a ubicar rápido qué
parte del proyecto tocó el commit.

Hay un check automático que valida el título del PR contra esta convención.

## Review

Nadie aprueba su propio PR. El review no es un trámite de jerarquía: existe porque
quien escribió el código ya no lo ve con ojos frescos.

## Flujo de labels en un issue

`status:needs-review` (recién creado) → `status:assigned` (tiene owner y arrancó) → `status:approved` (listo para PR).

## Templates

No se abren issues en blanco salvo que seas maintainer. Usa el template que
corresponda: bug, feature, o tarea asignada.

## Seguridad

- 2FA obligatorio para operar en la organización.
- Nunca compartir credenciales por chat. Van en un gestor de contraseñas o en Actions secrets.
- Nunca commitear tokens, API keys ni contraseñas. Si pasa: rotar primero, limpiar el historial después.

